pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'Code Dev pushed'
      }
    }

    stage('Test') {
      steps {
        git 'https://github.com/NaliniMano/Salesforce'
        bat 'bat mvn test'
      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Build Approval', id: 'Certify')
      }
    }

  }
}