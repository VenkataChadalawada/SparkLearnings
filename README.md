# SparkLearnings
A place you can learn spark from basics

How to Install in Mac:
Basic set up requires 

1. Install Apache Spark using Homebrew.
a. Install Homebrew if you don’t have it already by entering this from a terminal prompt:
/usr/bin/ruby -e "$(curl -fsSL
https://raw.githubusercontent.com/Homebrew/install/master/install)"
b. Enter brew install apache-spark
c. Create a log4j.properties file via
cd /usr/local/Cellar/apache-spark/2.0.0/libexec/conf
cp log4j.properties.template log4j.properties
(substituted 2.0.0 for the version actually installed)
d. Edit the log4j.properties file and change the log level from INFO to ERROR on
log4j.rootCategory.
2. Install the Scala IDE from http://scala-ide.org/download/sdk.html
3. Test it out!
a. Cd to the directory apache-spark was installed to (such as /usr/local/Cellar/apachespark/2.0.0/libexec/)
and then ls to get a directory listing.
b. Look for a text file we can play with, like README.md or CHANGES.txt
c. Enter spark-shell
d. At this point you should have a scala> prompt. If not, double check the steps above.
e. Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found)
f. Enter rdd.count()
g. You should get a count of the number of lines in that file! Congratulations, you just ran
your first Spark program!
h. Hit control-D to exit the spark shell, and close the console window
i. You’ve got everything set up! Hooray!

If you donot set up your Environment variables
        cd /usr/local/Cellar/apache-spark/2.1.0/libexec
        spark-shell 
The above syntax will get you into scala shell.

** - COPY ALL THE LIB FILES FROM JARS FOLDER INSIDE libexec folder into your project folder to get visibility for Scala Eclipse to add external jars under properties inorder to run a scala program

