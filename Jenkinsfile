pipeline{
    agent any

    stages{

        stage('checkout'){
            steps{
                git 'https://github.com/Priyadharshini155/devops-demo-project.git'
            }
        }

        stage('Build Docker Image'){
            steps{
                sh 'docker build -t priya-app:v1 .'
            }
        }

        stage('Deploy'){
            steps{
                sh 'docker rm -f priya-app || true'
                sh 'docker run -d --name priya-app -p 8081:80 priya-app:v1'
            }
        }
    }
}
