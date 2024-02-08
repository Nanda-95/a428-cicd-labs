pipeline {
    agent {
        docker {
            image 'node:14'  // Ganti dengan gambar Docker yang sesuai dengan kebutuhan aplikasi React Anda
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        // Tambahkan stage deploy jika diperlukan
    }
}
