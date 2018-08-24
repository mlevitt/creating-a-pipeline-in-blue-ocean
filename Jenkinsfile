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
        sh '''ls; \\
ls -al; \\
ls -al /var/run; \\
docker images || true'''
      }
    }
  }
}