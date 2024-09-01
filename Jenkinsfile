pipeline {
        agent{
        label 'NEW-SLAVE-LABEL'
        }
        stages {
            stage('Checkout') {
                steps {
                        checkout scm
                      }}
                stage('Build') {
                   steps {
                          sh 'JAVA_HOME=/home/ROHIT/SLAVEDIR/jdk-11.0.24 /home/ROHIT/SLAVEDIR/apache-maven-3.9.8/bin/mvn install'
                         }}
                stage('Deployment'){
                    steps {
                        sh 'cp webapps/pipeline-repo /home/ROHIT/SLAVEDIR/apache-tomcat-9.0.93'
                        }}
}}
