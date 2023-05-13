pipeline{
    agent any
    environment{
        sonarHome = tool 'sonarScanner'
    }
    stages{
        stage('Build'){
            steps{
            sh 'mvn clean package'
            }
        }
    stage ('Initialize & SonarQube Scan') {
        steps {
        withSonarQubeEnv('SonarQube') {
            sh 'mvn -X sonar:sonar'
            }
          }
        }
    }
}
