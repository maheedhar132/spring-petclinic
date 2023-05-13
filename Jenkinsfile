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
        withSonarQubeEnv('SonarQube') {
            mvn sonar:sonar
            }
          }
        }
    }
}
