pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
            sh 'mvn clean package'
            }
        }
        stage('Sonar Scan'){
            steps{
                sh 'echo "Hello"'
            }
        }
    }
}