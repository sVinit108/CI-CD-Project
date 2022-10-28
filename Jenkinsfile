pipeline {
  agent any
  stages {
    stage('Checkout-Code') {
      steps {
        git(url: 'https://github.com/sVinit108/CI-CD-Project', branch: 'main')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-Unit-Test') {
          steps {
            sh 'cd curriculum-front && npm i run test:unit'
          }
        }

      }
    }

  }
}