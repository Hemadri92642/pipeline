pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                git branch: 'main', url: 'https://github.com/Hemadri92642/pipeline.git'
                
                sh 'sudo cp -r index.nginx-debian.html /var/www/html/'
            }
        }
    }
}
