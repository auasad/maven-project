pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven : 'locatMVN'){
                    sh 'maven clean compile'
                }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven : 'locatMVN'){
                    sh 'maven test'
                }
            }
        }
        stage('Deployment Stage') {
            steps {
                withMaven(maven : 'locatMVN'){
                    sh 'maven deploy'
                }
            }
        }
    }
}