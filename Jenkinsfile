pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/achrafnejjari/test-jenkins.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac Test.java Test2.java'
            }
        }

        stage('Run Test.java') {
            steps {
                sh 'java Test'
            }
        }

        stage('Run Test2.java') {
            steps {
                sh 'java Test2'
            }
        }
    }

    post {
        success {
            echo "Pipeline exécuté avec succès !"
        }
        failure {
            echo "Erreur dans le pipeline !"
        }
    }
}
