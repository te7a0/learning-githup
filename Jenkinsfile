pipeline {
  agent any
  stages {
    stage('clean ') {
      steps {
        cleanWs()
      }
    }
    stage('checkout scm') {
      steps{
        git branch: 'main',
            url: 'https://github.com/te7a0/ci-cd-proj.-.git'
    }

  }
}
}
