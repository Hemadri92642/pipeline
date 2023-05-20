pipeline {
    agent any
    triggers {
        cron('H/2 * * * *')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                git branch: 'main', url: 'https://github.com/Hemadri92642/pipeline.git'
                
                sh 'sudo cp -r index.nginx-debian.html /var/www/html/'
            }
        }
        stage('URL status') {
            steps {
                sh 'curl -v http://ec2-34-203-31-180.compute-1.amazonaws.com/'
            }
        }
    }
}


