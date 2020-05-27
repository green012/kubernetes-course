### Secret

```
--> Save sensitive information ( db credentials )
--> we store secret outside of pod. They are stored in etcd database of master node
--> size max 1mb
--> secrets can be saved in form of env,volumes
--> only sent to target node

```


### secret --> manually, manifest file ( yml file)

```
kubectl create secret <type> <name> <data>

type --> generic
         docker-registry
         tls

data --> path to directory --> --from-file=
         keyvalue pair     -->  --from-literal=
         
```
