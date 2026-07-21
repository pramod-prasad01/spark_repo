# Spark installation in Mac
## 1. Install Java Prerequisites
### Install OpenJDK via Homebrew
>brew install openjdk

### Symlink it so the system wrapper can find it
>sudo ln -sfn /opt/homebrew/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk


## 2. Install Apache Spark
>brew install apache-spark

## 3. Configure Your Environment Variables
## Add Java and Spark configurations to your zsh profile
>echo 'export JAVA_HOME=$(/usr/libexec/java_home -v 17)' >> ~/.zshrc
>echo 'export SPARK_HOME="/opt/homebrew/opt/apache-spark/libexec"' >> ~/.zshrc
>echo 'export PATH="$SPARK_HOME/bin:$PATH"' >> ~/.zshrc

## Apply the changes to your current terminal session
>source ~/.zshrc


## 4. Update the Homebrew package database:
>brew update

## 5. Upgrade the Apache Spark :
>brew upgrade apache-spark


