pipeline {
    agent any

    stages {
        stage('connect') {
            steps {
                checkout scm
                echo 'Connected to Git Hub'
            }
        }
        stage('execute java') {
            steps {
                bat '''
                javac Prime.java
                java Prime
                '''
                echo 'Java Program executed Successfully!'
            }
        }
        stage('execute python') {
            steps {
                bat python sample.py
                echo 'Python program executed Successfully!'
            }
        }
        
    }
}
