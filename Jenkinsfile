pipeline {
    agent any
    
    tools {
        maven 'localMaven'
    }

    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebappi:${env.BUILD_ID}"
            }
        }
    }
}
