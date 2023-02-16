# Road-Steamer/CoP-Suite

This is the repository for RoadSteamer Cop-Suite, based on [Decidim](https://github.com/decidim/decidim).

### Requirements: 

1. Install **Docker** and **Docker-compose**
 
2. Clone this repository or [download and unpack it](https://github.com/Road-STEAMer/CoP-Suite/archive/refs/heads/main.zip) in some place.

```
git clone https://github.com/Road-STEAMer/CoP-Suite.git
```

### Running the application

Just open a terminal where you have cloned or downloaded this repository and execute:

```
docker-compose up
```
Point your browser to: http://localhost:3000

### Configuration external database for production environment
The database must be PostgreSQL 14.5.
To connect the app to an external database,in production, you have to configure all parameters into:
- docker-compose.yml

Into docker-compose.yml, into section "ENVIRONMENT" you have to set this parameter,
      DATABASE_URL="postgres://myuser:mypass@host:port/namedatabase"
      
      
      
### Deploy
Create your image:
```
docker build -t nameRepositoryDockerHub:tagname .
```
Just open a terminal where you have cloned or downloaded this repository and execute:

```
docker login -u username
```
Digit the password 


Copy the id of created image
```
docker images
```

```
docker tag idImages nomedockerhub:latest
```

Push your image into docker Hub:

```
docker push nomedockerhub:latest
```


Then you go on the server and pull your image:

```
docker login -u username
```
```
docker pull nomedockerhub:latest
```

Start the app:
```
docker run --rm -it -p 3000/3000/tcp nomedockerhub:latest
```



