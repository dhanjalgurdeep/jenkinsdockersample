pipeline {
    agent any
    tools{
      jdk 'localJDK'
      maven 'localMaven' 
    }
    stages { 
        stage ('Build') {
            steps {
                sh 'mvn clean package'
                sh "/Applications/Docker.app/Contents/Resources/bin/docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}