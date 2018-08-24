pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          environment {
            CI = 'true'
          }
          steps {
            sh './jenkins/scripts/test.sh'
          }
        }
        stage('') {
          steps {
            echo 'hello'
          }
        }
        stage('') {
          steps {
            input(message: 'Dave...', id: '1')
          }
        }
      }
    }
    stage('') {
      steps {
        echo 'goodbye'
      }
    }
  }
}