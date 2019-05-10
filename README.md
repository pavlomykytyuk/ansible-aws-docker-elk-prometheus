#Docker Swarm - WikiJS-FileBeat-Logstash-Kibana-ElasticSearch-Splunk-Prometheus-Grafana

Note: This project is only intended to present ideas.

In this project you will work with:
Log aggregation and analyzing tools(Splunk, Elastic Stack)
Monitoring tools (Prometheus, Splunk, Elastic Stack)
Dashboard and visualization tools (Grafana, Kibana, Splunk)
Configuration management tools Ansible

#How to test this?
1. Check ansible instalation
```
ansible --version
```
#2. After cloning this repo you should change and check AWS section with vars:
```
      region: us-west-2
      instance_type: t2.micro
      ami: ami-061392db613a6357b #aws
      keypair: pavlo.mykytyuk
      vpc_subnet_id: subnet-0cf73cb75c190fb50
      group: SecGroup for public network
``` 
#3. Configure Security Group.
Ports 22,80,3000,5000,5044,5601,2376,2377,7946,8000,8089,9090,9997,9100,9200,9300

#4. Run all containers with ansible
```
ansible-playbook -i ec2.py  ec2-ansible/global.yml
```

