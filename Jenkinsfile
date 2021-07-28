pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            
            
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat7(credentialsId: '18888c3c-e2f4-4db7-88ab-8b6605ef1f50',path: '', 
                url: 'http://3.17.204.104:8080/')], 
                contextPath: 'javawebproject', war: '**/java-web-project.war'
            }
            
            
        }
        
    }
    
    
}
