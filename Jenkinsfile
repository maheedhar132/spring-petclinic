pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
            sh 'mvn clean package'
            }
        }
    stage ('Initialize & SonarQube Scan') {
        steps {
        def scannerHome = tool 'sonarScanner';
        withSonarQubeEnv('My SonarQube Server') {
            mvn sonar:sonar
            }
          }
        }
    }
}
