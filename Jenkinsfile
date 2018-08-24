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
        stage('boring') {
          steps {
            echo 'hello'
          }
        }
        stage('Should I stay or should I go NOW!') {
          steps {
            input(message: 'Dave...', id: '1')
          }
        }
      }
    }
    stage('interesting') {
      steps {
        echo 'goodbye'
        echo 'goodbye'
      }
    }
  }
}
