docker_build:
	docker build -t wojciech12/talk-pywa-prom-flask .

start:
	docker-compose -f docker-compose.yaml --project-name talk-pywa-prom-flask up -d

stop:
	docker-compose -f docker-compose.yaml --project-name talk-pywa-prom-flask stop

prometheus_reload_config:
	curl 127.0.0.1:9090/-/reload -X POST

srv_random_trafic:
	curl 127.0.0.1:8080/hello ; \
	curl 127.0.0.1:8080/world ;
	
srv_random_trafic_complex_failed_db:
	curl 127.0.0.1:8080/complex?is_db_error=True

srv_random_trafic_complex_slow_db_and_svc:
	curl '127.0.0.1:8080/complex?db_sleep=3&srv_sleep=2'

srv_random_trafic_complex_failed_third_party:
	curl 127.0.0.1:8080/complex?is_srv_error=True
