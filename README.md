# install strimzi cluster operator
`helm upgrade --install strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system --version 0.41.0 --set watchAnyNamespace=true --create-namespace`
# uninstall strimzi cluster operator
`helm uninstall strimzi-kafka-operator strimzi/strimzi-kafka-operator --namespace strimzi-system`
# installation of kafka and zookeeper
`cd application`

`./deploy_smo_from_repo.sh`

# uninstall onap
`helm undeploy onap -n onap

for topic in $$(kubectl get kafkatopic -n onap -o name); do   kubectl patch $$topic -n onap -type=json -p '[{"op": "remove", "path": "/metadata/finalizers"}]'; done

kubectl delete ns onap

sudo rm -rf /dockerdata-nfs/onap`
