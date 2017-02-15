#This benchmark was run against a sample of 71K publications taken from PubMed (ftp://ftp.ncbi.nlm.nih.gov/pub/pmc)

The job was lanched as follows:

```shell
SPARK_HOME=
$SPARK_HOME/bin/spark-shell --master local[4] -i taccession.scala
$SPARK_HOME/bin/spark-shell --master local[16] -i taccession.scala
$SPARK_HOME/bin/spark-shell --master local[32] -i taccession.scala

$SPARK_HOME/bin/spark-shell --master spark:$master:7070 -i taccession.scala
```