pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven : 'locatMVN') {
                    sh 'mvn clean compile'
                }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven : 'locatMVN') {
                    sh 'mvn test'
                }
        }
        stage('Deploying Stage') {
            steps {
                withMaven(maven : 'locatMVN') {
                    sh 'mvn deploy'
                }
        }
    }
