pipeline {
    agent any

    tools {
        maven 'Maven-3.6.3'  // 👈 matches your Jenkins tool config
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-pat', url: 'https://github.com/suresh777777/my-java-app.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}

