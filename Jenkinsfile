pipeline{
    agent any
    stages{
        stage('Build'){
            sh 'mvn clean package'
        }
        stage('Sonar Scan'){}
    }
}