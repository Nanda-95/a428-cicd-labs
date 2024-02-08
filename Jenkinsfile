node {
    stage('Setup Environment') {
        // Instal Node.js dan npm jika belum terinstal
        sh 'apt-get update && apt-get install -y nodejs npm'

        // Tambahkan npm ke PATH
        script {
            def npmBin = sh(script: 'which npm', returnStdout: true).trim()
            env.PATH = "${npmBin}:${env.PATH}"
        }
    }

    stage('Checkout') {
        checkout scm
    }

    stage('Build') {
        sh 'npm install'
    }

    // Sisanya dari Jenkinsfile
}
