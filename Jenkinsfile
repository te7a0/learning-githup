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
    stage('Maven Test') {
            steps {
                // يشغل اختبارات Maven
                sh 'mvn test'
            }
        }

        stage('Maven Install') {
            steps {
                // يبني المشروع ويضيف artifact للـ local repo
                sh 'mvn install'
            }
        }
  }
}
