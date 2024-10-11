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
                               sh 'mvn dependency:purge-local-repository'   
                               sh 'mvn clean package'
                          }
                 }

                 stage ("building docker image") {
                          steps {
                                sh 'sudo  docker build -t java-app:$BUILD_TAG .'
                          }
                 }
        }  
 }

