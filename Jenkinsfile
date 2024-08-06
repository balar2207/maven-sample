pipeline {
    agent any
    stages {
        stage('Git Clone') {
            steps {
                git 'https://github.com/balar2207/maven-sample.git'
            }
            
        }
        stage('Maven Build') {
            steps {
                sh 'mvn clean package deploy' 
            }
            
        }
        stage('Deploying to Tomcat') {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'jenkins', path: '', url: 'http://192.168.1.57:8080')], contextPath: 'devops123', war: '**/*.war'
            }
            
        }
        
    }
    
}
