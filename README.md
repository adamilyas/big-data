# CS-E4640 - Big Data Platforms, 12.09.2018-20.12.2018
https://mycourses.aalto.fi/course/view.php?id=20599

This course focuses on advanced scalable cloud
computing technologies and on key algorithmic ideas and
methods used to implement them.

# Install java
____

check if java is installed
`$ java -version`

if not installed, download jdk at https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
(for windows, dont forget to add to path in SYSTEM ENVIRONMENT (google pls))

for linux, you may download jdk via terminal$:
`$ sudo apt-get update`
`$ sudo apt-get install default-jdk`

# Install scala-sbt
____
http://www.scala-sbt.org/0.13/docs/Setup.html

Test by launching
`$ sbt console`


## File structure
_____

src/
  main/
    resources/
       <files to include in main jar here>
    scala/
       <main Scala sources>
    java/
       <main Java sources>
  test/
    resources
       <files to include in test jar here>
    scala/
       <test Scala sources>
    java/
       <test Java sources>

`.gitignore` should contain `/target`

`$ cd assignmentX`
`$ sbt test`
`$ sbt download`

`$ sbt run`

# Install spark
_____
https://spark.apache.org/downloads.html
Download Spark: spark-2.4.0-bin-hadoop2.7.tgz 
i like to extract to /home/{yourname}/

Check if spark works
`$ cd spark-2.4.0-bin-hadoop2.7/bin`
`$ ./spark-shell`

Now to configure path and alias (UBUNTU)
add the following to ur `.bashrc` file 
(change the path file according if you didnt extract to `home/{yourname}/`)

```
# so that u can access spark from terminal
`alias spark='~/spark-2.4.0-bin-hadoop2.7/bin/spark-shell'`

# spark path (based on your computer)
`export SPARK_HOME="/home/{yourname}/spark-2.4.0-bin-hadoop2.7"`
```

# Use scala kernel in Jupyter notebook
____
`$ pip install spylon-kernel`
`$ python -m spylon_kernel install --user`

# Install scala (Optional)
_____
for linux,
`$ sudo apt-get install scala`
`$ scala`
