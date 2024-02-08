pipeline {
    agent any
    
    stages {
        stage('Debug') {
            steps {
                script {
                    sh 'echo $PATH'
                    sh 'which docker'
                    sh 'docker --version'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Pull Docker image
                    docker.image('node:14').pull()

                    // Debugging
                    sh 'docker images'

                    // Run Docker container
                    def container = docker.image('node:14').run('-v $PWD:/app', 'npm install')

                    // Debugging
                    sh "docker ps -a"
                    
                    // Log container output
                    container.withRun { c ->
                        sh "docker logs ${c.id}"
                    }
                }
            }
        }
    }
}
