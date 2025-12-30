pipeline {
    agent any

    // نحدد الأدوات اللي أضفناها في Jenkins
    tools {
        jdk 'java-3'
        maven 'maven-3'
    }

    stages {

        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Checkout SCM') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/te7a0/ci-cd-proj.-.git'
            }
        }

        stage('Maven Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Maven Install') {
            steps {
                sh 'mvn install'
            }
        }

    }
