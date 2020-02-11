#!make
APP_NAME=prometheus

build:
	docker build -t ${APP_NAME} .

run:
	docker run --rm -ti -p 9090:9090 \
	--name ${APP_NAME} \
	${APP_NAME} \
	--config.file=/etc/prometheus/prometheus.yml
