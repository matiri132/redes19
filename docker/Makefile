setup:
	docker-compose -p tp6 up -d
	
clean:
	docker-compose -p tp6 down;

routes:
	docker exec -ti tp6_r1_1 ip route del default;
	docker exec -ti tp6_dns-bind9_1 ip route del default;
	docker exec -ti tp6_dns-bind9_1 ip route add default via 200.18.13.2;
	docker exec -ti tp6_host1_1 ip route del default;
	docker exec -ti tp6_host1_1 ip route add default via 200.18.12.2;
	
r1:
	docker exec -ti tp6_r1_1 ash;

dns:
	docker exec -ti tp6_dns-bind9_1 /bin/bash;	

host:
	docker exec -ti tp6_host1_1 ash;

