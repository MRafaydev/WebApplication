pipeline{
    agent any
    stages{
        agent {
            docker {
                image 'openjdk:11'
            
            }
        }
        stage("Sonar Quality Check"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
                    }
                }
            
            }
    
        }
    }
}