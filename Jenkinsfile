pipeline {
    agent any

    tools {
        nodejs "NodeJS"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    npm 'install'
                }
            }
        }

        // Tambahkan tahapan lain jika diperlukan
    }
}
