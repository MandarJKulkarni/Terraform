Pplaceholder for some of the helm commands (Until I do something meaningful with them)

Commands for installing backstage via helm chart on a K8S cluster

	helm repo add bitnami https://charts.bitnami.com/bitnami
	helm repo add backstage https://backstage.github.io/charts
	helm repo list ==> to verify that backstage and bitnami repos are listed
	helm search repo backstage ==> to get the name of the chart
	
	helm install backstage backstage/backstage ==> to install the backstage deployment
	
	Then "kubectl get services" => to get the backstage service name
	
	then port-forward "kubectl port-forward svc/backstage 8080:7007" => to forward the backstage service on port 8080 of your localhost
	
	Then browse to localhost:8080
	
	
	other useful helm commands:
		helm list
		helm list --short
		helm env
		helm get manifest backstage		==> to see what all components are deployed
		helm upgrade backstage backstage/backstage
		helm status backstage
		helm rollback backstage 1
		helm history backstage ==> to check the history of a release
