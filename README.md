`helm upgrade --install strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system --version 0.35.0 --set watchAnyNamespace=true --create-namespace`

`helm uninstall strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system`

`cd application`

`./deploy_smo_from_repo.sh`
