# spark-examples
Run example application of Apache Spark. A self learning exercise.

## Get Spark Binaries
```sh
$ wget http://mirrors.estointernet.in/apache/spark/spark-2.4.0/spark-2.4.0-bin-hadoop2.7.tgz
$ tar -xvf spark-2.4.0-bin-hadoop2.7.tgz
$ export SPARK_HOME="$(pwd)/spark-2.4.0-bin-hadoop2.7"
```

## Start Spark (standalone) MASTER and WORKER
```sh
$ $SPARK_HOME/sbin/start-master.sh
...
...
..... checkout http://localhost:8080/

$ export SPARK_MASTER=spark://your-host:7077

$ $SPARK_HOME/sbin/start-slave.sh $SPARK_MASTER
```

## Run an example application from pre-defined examples
```sh
$ $SPARK_HOME/bin/spark-submit --class org.apache.spark.examples.SparkPi --master spark://shiva-pc:7077 --executor-memory 2G --total-executor-cores 4 $SPARK_HOME/examples/jars/spark-examples_2.11-2.4.0.jar 5000
```

