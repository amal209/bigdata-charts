# BigData Helm charts

Curated Big Data charts for Kubernetes.

## Install chart from helm repository

charts in `charts/`` folder are packaged and available at Gradiant's helm repo:  

[https://gradiant.github.io/bigdata-charts/](https://gradiant.github.io/bigdata-charts/)

You can add the helm repo to your Helm CLI:

```bash
helm repo add bigdata-gradiant https://gradiant.github.io/bigdata-charts/
```

Then you have a collection of charts available to install. For example, to install hdfs:

```bash
helm install --name hdfs bigdata-gradiant/hdfs
```


# Install Jupyter
In the actual jupyter chart the image that is used doesn't contain JAVA
## to change it with another image that contain java: 
* Go to jupyter chart
* in values.yaml change actual image TO:

image:

  registry: docker.io
  
  repository: jupyter/pyspark-notebook
 
  tag: java-11.0.15
![image](https://user-images.githubusercontent.com/57093156/167864980-a5269bc2-0815-47e1-9a20-b55c1580605a.png)

## For more Jupyter images and tags
Go TO https://hub.docker.com/r/jupyter/pyspark-notebook/tags
