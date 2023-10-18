.PHONY: cluster-up cluster-down docker-build docker-run jupyter-client 
cluster-up:
		kind create cluster --config cluster.yaml

cluster-down:
		kind delete cluster

docker-build:
		docker build . -t langserve-operator-server

docker-run:
		docker run --rm -e "OPENAI_API_KEY=$$OPENAI_API_KEY" -p 8000:8000 langserve-operator-server

jupyter-client:
		jupyter-notebook ./client.ipynb

