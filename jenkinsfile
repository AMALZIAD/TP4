pipeline{

    agent any

    environment {
        DOCKERHUB_CREDENTIALS=credentials('dockerHubSchool')
    }

    stages {
        
        stage('gitclone') {

            steps {
                git 'https://github.com/AMALZIAD/TP4.git'
            }
        }

        stage('Build') {

            steps {
                bat 'docker run -d -p 8082:80 aymlen/tp4:latest .'
            }
        }

        stage('Test') {
            
            steps {
                bat 'docker --version'
            }
         }
         stage('Deploy') {
            
            steps {
                echo 'Delpoyement ....'
            }
         }   
        stage('Push') {

            steps {
                bat 'docker push aymlen/tp4:latest'
            }
        }
    }

}
