pipeline{
    agent any  

    stages{
        stage('github'){
            steps{
                git credentialsId: 'github_app', url: 'https://github.com/saranyaAWS/samplemaven.git'
            }
        }
        stage('build'){
            steps{
               echo "build start"
               sh 'mvn clean compile'
            }
        }
        
        stage('test'){
            steps{
                echo "testing"
                sh 'mvn test'
            }
        }
        stage('deploy'){
            steps{
                echo "Running java program"
                sh 'java -cp target/classes App'
            }
        }

    }
}
