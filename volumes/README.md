# Create volumes

## Create Volume in AWS

```
aws ec2 create-volume --size 10 --region your-region --availability-zone your-zone --volume-type gp2 --tag-specifications 'ResourceType=volume, Tags=[{Key= KubernetesCluster, Value=kubernetes.domain.tld}]'
```
# Volumes --> deploy applications with state --> with state = applications write/create files locally, we save that in volumes

``` 
save the state ( data ) outside of the container.

attach a volume the container, even if the container stops or kills, you still have the data.

you can have volumes outside of cluster, using the plugins.
```

### Usage of volumes
```
 You must create an EBS volume using aws ec2 create-volume or the AWS API before you can use it
```

### For AWS EBS

```

There are some restrictions when using an awsElasticBlockStore volume:

the nodes on which Pods are running must be AWS EC2 instances
those instances need to be in the same region and availability-zone as the EBS volume
EBS only supports a single EC2 instance mounting a volume

```

### Use kubectl drain command

```
The node will delete everthing it has on it and will not be ready for any another scheduling

kubectl get nodes
kubectl drain <node name>

Once your work is done, you can make your node available for scheduling

kubectl uncordon <node name>
```

### Use case for kubectl drain

```
- do maintenance on node
- testing purposes

```
