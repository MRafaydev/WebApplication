pipeline{
    agent any
    stages{
        stage("Sonar Quality Check"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        bat'chmod +x gradlew'
                        bat'./gradlew sonarqube'
                    }
                }
            
            }
    
        }
    }
}