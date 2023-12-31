# Spark with IntelliJ Community

https://www.youtube.com/@hackprotech/videos

## 1. Download Spark

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/bf4f7471-5ff8-4158-a5e8-d63b89ddc1cc)

Unzip the "spark-3.5.0-bin-hadoop3.tgz"

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/39fbee24-681a-47e3-8f63-baea221ec099)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/3bca82b7-b6e9-4124-b3a4-75506da8395a)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/8353cd13-5d6c-4d72-bf18-337796c3e8ff)

## 1. Download winutils for Hadoop

Go to this repository and download it

https://github.com/kontext-tech/winutils

Once downloaded the winutils repository, Unzip the file

![image](https://github.com/luiscoco/Spark_with_IntelliJ_Community/assets/32194879/466d9fe0-2020-4105-9cef-8e9b1f692f47)

Now we cut from the Download folder and we copy it to the C:/ root

![image](https://github.com/luiscoco/Spark_with_IntelliJ_Community/assets/32194879/2ef99063-4dd9-4879-996c-9a04dc8e2cff)

In the following section we have to set the HADOOP_HOME environmental variable

## 2. Set Spark environmental variable

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/993e30be-d134-4364-bd56-1135dcf6084a)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/17011565-587c-4b1a-98f7-5313cf4b21c2)

## 2. Set Hadoop winutils environmental variable

We navigate to the bin folder where is located the winutils.exe file. This path will be copied later in the HADOOP_HOME environmental variable.

![image](https://github.com/luiscoco/Spark_with_IntelliJ_Community/assets/32194879/e10cd456-b8ca-4498-88bb-dbceff907653)

We create a new environmental variable called HADOOP_HOME and we set the value to the path where is located the bin folder, as explained above

![image](https://github.com/luiscoco/Spark_with_IntelliJ_Community/assets/32194879/7197a63d-e505-4c7d-a5d6-8fe8a8eff432)

We add the path to the winutils.exe file in the PATH environmental variable

![image](https://github.com/luiscoco/Spark_with_IntelliJ_Community/assets/32194879/b4e04093-3d9f-4f6e-9b7e-a61c3b3fc2aa)

## 3. Check the spark-shell is installed

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/e453931d-da41-4204-a750-a8c416121322)


## 4. Install IntelliJ Community Edition

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/b86a6bf1-1217-46b1-bc82-ffc584830f1f)

## 5. Create a new Scala project with IntelliJ

Run IntelliJ Community and confirm "Scala" plugin is installed

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/b3b48661-b32f-426a-af10-e2312afa3456)

Select "Projects" in the left menu, and then click on the "New Project" button

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/ffe80d72-07af-4e9b-ba30-e48318482982)

Before we input the new project data, copy Spark version and the Scala Version

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/55573bfe-cf67-4f32-8534-e2c92cc4fcef)

Then we input the new project data

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/3d1d8dd3-8cae-4932-bd7c-d4a1038f3903)

## 6. Set the build.sbt file

```
ThisBuild / version := "0.1.0-SNAPSHOT"

ThisBuild / scalaVersion := "2.12.18"

lazy val root = (project in file("."))
  .settings(
    name := "FirstSparkProject"
  )

// https://mvnrepository.com/artifact/org.apache.spark/spark-core
libraryDependencies += "org.apache.spark" %% "spark-core" % "3.5.0"
```

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/b4b3838e-147a-4111-87df-48c942c79e42)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/85117f86-4a8c-4ce6-8683-d241437242b3)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/0149631a-5d52-4a53-b89d-31dfd9371b14)

Press the "sbt" button and also press the button "Reload sbt projects" to load the spark library dependency

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/9b9c99c2-86cb-40e3-b292-3d4ce8bf29df)

We check the project was reloaded with all the dependencies including the new spark dependency

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/e0b101de-e575-423e-9d2a-df91ae7db669)

## 7. Create a package and the scala source code file

First we create a new package

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/e675b594-0690-4852-8ec1-8f3c82f889f0)

We set the new package name

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/55749e04-a357-4240-821a-c2fa7a0a2107)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/8a9ac4a4-c773-4f00-92a2-c9a282c66e20)

We create a new scala Object

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/c28d6a7c-0074-4db1-853a-1287ae59693f)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/d20c98af-5452-400c-b37d-30681e8ab6ff)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/8f977ba6-bb0d-41ae-a978-df18d448082a)

## 8. We enter the spark main file code

We first extends the object from the App

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/441e66da-c5cb-4bac-95c8-0b86842fdfc3)

Then we enter the rest of the code

```scala
package com.luispackage

import org.apache.spark.{SparkConf, SparkContext}

object HelloWorld extends App {

  // Set up Spark configuration
  private val conf = new SparkConf().setAppName("HelloSpark").setMaster("local[*]")

  // Create a Spark context
  private val sc = new SparkContext(conf)

  // Actual Spark code here
  private val helloRDD = sc.parallelize(Seq("Hello", "Spark"))
  helloRDD.foreach(println)

  // Stop the Spark context
  sc.stop()
}
```

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/1b6e0fb3-1361-4f59-8aee-fbc05d5f1128)

## 9. How to run the spark scala application

We right click on the scala code and select the "Run HelloWorld"

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/52d93e7d-dcbc-46be-a92e-c3be43bd9d72)

This is the run output

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/6fc15e60-9cc0-47ac-87cb-acbc917d818d)

Also see the Process finished with exit code 0

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/372ba1e6-4fa1-47a8-9ff1-17e98c55de55)

## 10. Another scala spark application sample

This is the new application source code:

```scala
package com.luispackage

import org.apache.spark.{SparkConf, SparkContext}

object HelloWorld extends App {
  private val sparkContext = new SparkContext(master = "local", appName = "Hello World")
  private val sourceRDD = sparkContext.textFile(path = "C:\\Users\\luisc\\Downloads\\testFile.txt")
  sourceRDD.take(num = 10).foreach(println)
}
```

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/6c2f4726-6b70-4b4b-93f9-7a802071e425)

We also create the testFile.txt

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/78f430a9-5d15-41a6-9356-afb401932a39)

Now we run the application

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/90d02ea7-382b-41ed-a850-5dd6df7143c4)

![image](https://github.com/luiscoco/Spark_videos/assets/32194879/9fe626de-4258-4d71-a7d9-9894aec12ba1)
