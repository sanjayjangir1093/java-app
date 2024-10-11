pipeline {
        agent any
        stages {
                 stage ("pull code from git repo") {
                          steps {
                                git branch: 'main', url: 'https://github.com/sanjayjangir1093/java-app.git'
                                }
                        }
                 stage ("build the code") {
                          steps{
                               bat 'sudo  mvn dependency:purge-local-repository'   
                               bat 'sudo mvn clean package'
                          }
                 }

                 stage ("building docker image") {
                          steps {
                                bat 'sudo  docker build -t java-app:$BUILD_TAG .'
                          }
                 }
        }  
 }

