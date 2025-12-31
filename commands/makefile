download:
	kubectl apply -f k8s/jobs/jetclass-download.yaml
	kubectl apply -f k8s/jobs/quarkgluon-download.yaml
	kubectl apply -f k8s/jobs/toplandscape-download.yaml

redeploy: 
	kubectl rollout restart deployment infra-jupyter
	kubectl rollout restart deployment infra-mlflow
	kubectl rollout restart deployment infra-browser
	kubectl rollout restart deployment infra-dashboard
	kubectl rollout restart deployment infra-file-browser

nuke:
	kubectl delete -f k8s/

healthcheck:
	kubectl apply -f k8s/tests/tests-infra-healthcheck.yaml
