pipeline {
  agent any
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