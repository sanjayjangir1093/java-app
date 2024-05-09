pipeline {
        agent any
        stages {
                 stage ("pull code from git repo") {
                          step {
                                git branch: 'main', credentialsId: 'docker', url: 'https://github.com/sanjayjangir1093/java-app.git'
                                }
                        }
}
                 stage ("build the code") {
                          step{
                               sh 'sudo mvn dependency:purge-local-repository'
                               sh 'sudo mvn clean packge
                          }
                 }

                 stage ("building docker image") {
                          step {
                                sh 'docker build -t java-app:$BUILD-TAG .
                          }
                 }
~
~
~

