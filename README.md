# Wordpress Multisite On GKE


### TO-DO:

- [x] deploy wordpress
- [x] wordpress patching // fix erros
- [ ] Converte To Multi Site using patching use mtahle/wordpress:ms
- [x] wordpress with persistant disk
- [x] wordpress with CloudSQL




#### Update a container's image; spec.containers[*].name is required because it's a merge key

``` kubectl patch pod wordpress-5c8c5d94c9-56fk2 -p '{"spec":{"containers":[{"name":"wordpress","image":"mtahle/wordpress:ms"}]}}' ``` 


#### create secrets 

~~~~ kubectl create secret generic cloudsql-db-credentials --from-literal=username=wp --from-literal=password=wp
 kubectl create secret generic cloudsql-instance-credentials --from-file=credentials.json=terrafrom-learning-3c3bfb7d6a47.json ~~~~ 
