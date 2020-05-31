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
creates the volumes and attach it to the pod

```
