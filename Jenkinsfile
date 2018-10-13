pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
      steps {
        sh 'file 18'
      }
    }
    stage('Test') {
      post {
        always {
          junit 'target/surefire-reports/*.xml'

        }

      }
      steps {
        sh 'mvn test'
      }
    }
  }
  tools {
    maven 'maven'
    jdk 'jdk'
  }
}
