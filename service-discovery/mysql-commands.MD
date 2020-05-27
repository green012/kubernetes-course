### Get into the database container

``` 
 kubectl exec -it <pod> -- bash
 
 you will be in the pod
 
 mysql -u root -p < enter the password you've set in secrets'
 
 show databases;
 
 use < database which is created >;
 
 show tables;
 
 select * from <table>
 
 ```
