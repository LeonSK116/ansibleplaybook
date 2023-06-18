## Based on microsoft/AnsibleLabs Repository
With some adjustment to make it work on Ansible controller.

- Code is from https://github.com/dansand71/nodejs-todo

### Ansible
To install Azure collection hosted in Galaxy:

```
ansible-galaxy collection install azure.azcollection
```

Install dependencies required by the collection (adjust path to collection if necessary):

```
pip3 install -r ~/.ansible/collections/ansible_collections/azure/azcollection/requirements-azure.txt
```
OR

```
pip3.x install -r ~/.ansible/collections/ansible_collections/azure/azcollection/requirements-azure.txt
```


### Mongo Test
[Azure Cosmos DB Explorer](https://cosmos.azure.com/).
[Work with data using Azure Cosmos DB Explorer](https://learn.microsoft.com/en-us/azure/cosmos-db/data-explorer).

MongoDB Basics 
[Basic commands for mongoDB](https://blog.e-zest.com/basic-commands-for-mongodb).

Show DB

```show dbs```

Create new database
To create a new database execute the following command.
```use DATABASE_NAME```


Know your current selected database
To know your current working/selected database execute the following command

```db```

Drop database
To drop the database execute following command, this will drop the selected database

```db.dropDatabase()```


### <u>Nodejs</u>
Conenct DB

```
var dbURI = "mongodb://127.0.0.1:27017/DB_NAME";
```

```
mongoose.connect('mongodb://127.0.0.1/DB_NAME')
```


Build and run container

```
git clone https://github.com/LeonSK116/nodejs-todo.git
```

```
podman build -t nodejs-todo .
```
OR
```
podman pull quay.io/redhat_leonsk/nodejs-todo
```

```
podman run -itd -e MONGO_DBCONNECTION= --name todo-app IMGAE_NAME:latest
```

```
podman tag localhost/nodejs-todo XXX.azurecr.io/demo/nodejs-todo
```

```
podman push XXX.azurecr.io/ossdemo/nodejs-to
```
