
# Running the project  
You should have docker installed in You system/server, If running in system then go to http://localhost:8888/notebooks/work/test32.ipynb else http://server.ip:8888/notebooks/work/test32.ipynb  
  
To start the docker run the following command  
````
$ docker run -it -p 8888:8888 -v $(pwd):/home/jovyan/work/ --rm --name jpy  jupyter/pyspark-notebook | grep token 
```` 
#### Use the token from terminal , something like 
````  
$ data docker run -it -p 8888:8888 -v $(pwd):/home/jovyan/work/ --rm  --name jpy  jupyter/pyspark-notebook | grep token  
[I 09:01:22.907 NotebookApp] http://0fa6523d10ef:8888/?token=e272925a91a1b0ec4833fb253aed10892212218adf98b7cd  
[I 09:01:22.907 NotebookApp]  or http://127.0.0.1:8888/?token=e272925a91a1b0ec4833fb253aed10892212218adf98b7cd  
 http://0fa6523d10ef:8888/?token=e272925a91a1b0ec4833fb253aed10892212218adf98b7cd or http://127.0.0.1:8888/?token=e272925a91a1b0ec4833fb253aed10892212218adf98b7cd
 ````  
 to login into jupyter and browse to above mentioned notebook, run all the cells and navigate to <b>$(pwd)/output_path/<b> directory in the project directory, You can get the oup Json files there  
  
#### Special thanks to the docker image I am using, You can read about it <br>@ https://github.com/jupyter/docker-stacks/tree/master/pyspark-notebook <br>It has spark standalone and jupyter built in it
