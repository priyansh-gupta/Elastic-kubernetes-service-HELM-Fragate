# Elastic-kubernetes-service-HELM-Fragate
### Day1
1. AWS provides EKS stands for #Elastic_Kubernetes_Service which is a great container and cluster management service which uses Kubernete behind the scene.
2. for deploying any App or website we require an OS and server necessary for it which is called environment. We need to launch this environment on some bare metal setup or on containers so that deployment is fast and easy to manage. We also need some physical resources like CPU and ram which we can buy or either we take them on rent as we are using on AWS like in EC2.
3. the working and architecture of Docker container and engine, how it work on the resources similarly understand that #kubernetes which is a container management engine that behind the scene uses docker engine to launch pods and container that has our app or website running.
4. the architecture of Kubernetes Cluster which is the most important part of this training. In Kubenetes Cluster we generall have master and slave node where slave done the task given by master. This setup has these major components: api-client, kubeclt, schedulers, etcd, kubelet.
5. the architecture of ElasticKubernetesService and understand its working and use cases in real world. 
6. how to create an IAM account which is need for working with EKS.
7. to work with AWS and EKS we have these ways:
i) WebUI
ii) CLI and for cli which as AWS EKS command and other is eksctl
iii) Terraform
8. the User/Admin need to specify the EKS about the type of instances means what are the requirements and configuration of resources need. So for this we need to tell the node groups we need for our requirements like for instance which image, storage type is required.
9. to create a desire to have 3 slaves nodes in two different groups with different types and some region and all these thing we put in a yml file.
10. eksctl command create a eks cluster and behind the scene Eks cluster goes to ec2 to launch instances or eksctl goes to the cloud formation who will create all the stacks. But first of all a master is created after that slave launches.
11. we launched a deployment over the nodes with some replicas which are running on different datacenters of Mumbai region of availability zone.
12. our cluster setup is quiet similar as VPC or subnet where we have two nodes running in 2 different labs.
13. the concept of load balance which is important resource and service need to manage the traffic that come to any website or app. It will also expose the service for outside the world.
14. the entire Infrastructure is provided by AWS and kubernetes who manage the nodes and cluster.
15. the pods are ephemeral in nature so if pods get deleted by any error or some other reason then new pod of similar kind launch on the go but the entire data will be lost. So we need a storage for peramanent or persistent storage.
16. the concept of PersistentVolumeClaim and PersistentVolume and it contact to storage class that actually provide the storage from different kind of storage like SAN, EBS, Ceph etc.
17. that by default the storage class is gp2 but we can change it our desired storage class like IOPS. We also set our default pvc to our own created pv storage.



### Day2
1. the pure configuration of EKS is entirely handle by Kubernetes master. It launches the instances with some constraints that is what type of instance we need like t2.micro or t2.small or what type of volume require EBS or S3 or what is the costing of usage or on-demand and rest of the management done by EKS.
2. We can also make some customisation like we can use Windows worker node and also use spot instances and make some auto-scaling either manually or using some program.
3. We EKS is good for managing multiple EC2, EBS, EFS, ELB and on AWS we can reate our own EC2 cluster and manage it our own or it can be managed by EKS. but it has sime limitations that it can integrate only internal service like ELB.
4. If we want to integrate our own services so we need to create our own cluster with Kubernetes. In our own cluster we can put any type of required resource as per the need.
5. we need AWS can manage the cluster so that Admin/User doesn't need to worry about any of service, master node or slave node. It is a kind of serverless architecutre for contanier management and known as Fargate in AWS.
6. In AWS only two serivces is meant for using the containers one in ECS and other is EKS. Fargate is good for provide the services if required as in on-demand services and create serverless architecture also for these on-demand service.
7. using t2.micro we can launch only 4 pods in nodes but with t2.small we can launch 11 pods in the same nodes.
8. the containers have default behaviour so that they can communicate with other container of the same nodes this is bcoz of overlay-network and can be done by using some plugins called flannel.
9. if we want that two different containers or cluster can connect with each other so for this we require a CNI which is a program that use plugins for connections between the two.
10. AWS use some internal CNI plugins so that there is a proper connectivity between different cluster and the nodes running inside these cluster.
11. the architecutre of VPN which has multiple labs called subnets which contains our cluster and instances and in the subnet for communication an ENI is required. ENI is meant for the connection between different subnets.
12. when we run EKSCTL command to create the cluster behind the scene it calls the CLoudFormation which contacts the different services for creating the cluster. It contact to VPC,EC2, EBS, ENI and after that it creates the cluster.
13. the concept of ROLE which is an internal security services provided by AWS and it doesn't work outside the AWS. It is use accessing the AWS account, launching the instance, making new user for the account.
14. about the HELM which is Hub similar like Docker Hub which provide man y Kubernetes images for running pods like Jenkins stable image, SQL images etc.
15. how to use prometheus and garafana on Kubernetes. We launch pods for prometheus and grafana using different namespaces.

### by PRYANSH GUPTA
