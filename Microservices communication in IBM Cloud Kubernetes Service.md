
# Microservices communication in IBM Cloud Kubernetes Service
The standard these days is REST and really JSON/REST, so use that. For asynchronous integration, follow an open, cloud-friendly standard like IBM Message Hub with Apache Kafka. Other examples of asynchronous protocols are AMQP, MQ Light, RabbitMQ.

When you create a Kubernetes cluster in IBM Cloud Kubernetes Service, every cluster must be connected to a public VLAN(virtual local area networks). The public VLAN determines the public IP address that is assigned to a worker node during cluster creation.

The public network interface for the worker nodes is protected by Calico network policies. These policies block most inbound traffic by default. However, inbound traffic that is necessary for Kubernetes to function is allowed, as are connections to NodePort, Loadbalancer, and Ingress services. NodePort is an easy way to start with simple public access to apps. As you progress to more sophisticated networking, the LoadBalancer gives you some portable public and private IP addresses. And when you grow to a larger microservices implementation, Ingress provides routing for multiple apps across HTTPS, TCP, or UDP load balancer. 
<img src='https://courses.cognitiveclass.ai/assets/courseware/v1/94ec891e5cb289a90ad44bee1d5afc8a/asset-v1:CognitiveClass+CO0301EN+v1+type@asset+block/dwc024_decision_tree.png' width = 500/>
## IBM Message Hub service
IBM Cloud has a messaging system service called IBM Message Hub. It’s based on the Apache Kafka project, which is rapidly becoming a standard for high-volume messaging on cloud platforms.
It’s used to integrate lots of services in cloud, but you can also use it to integrate your apps and microservices running in IBM Cloud. It supports two APIs: a simple HTTP REST API and a more complex but more powerful Kafka API.
