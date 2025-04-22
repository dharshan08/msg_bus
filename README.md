# install strimzi cluster operator
`helm upgrade --install strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system --version 0.41.0 --set watchAnyNamespace=true --create-namespace`
# uninstall strimzi cluster operator
`helm uninstall strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system`
# installation of kafka and zookeeper
`cd application`

`./deploy_smo_from_repo.sh`
