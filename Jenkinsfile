pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''ls; \\
ls -al; \\
docker images || true'''
      }
    }
  }
}