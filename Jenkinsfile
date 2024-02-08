pipeline {
    agent any

    tools {
        nodejs "Nama_NodeJS_Installation" // Ganti dengan nama instalasi NodeJS yang ada di Jenkins
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
                    // Tambahkan langkah-langkah untuk build aplikasi Node.js di sini
                    sh 'npm install'
                    // ... tambahkan perintah-perintah lain yang diperlukan
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Tambahkan langkah-langkah untuk test aplikasi Node.js di sini
                    sh 'npm test'
                    // ... tambahkan perintah-perintah lain yang diperlukan
                }
            }
        }

        // stage('Deploy') {
        //     steps {
        //         script {
        //             // Tambahkan langkah-langkah untuk deployment aplikasi Node.js di sini
        //         }
        //     }
        // }
    }
}
