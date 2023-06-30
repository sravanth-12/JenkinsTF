pipeline {
    agent any
     stages {
        stage('Git checkout') {
           steps{
           git branch: 'main', credentialsId: 'bdad8339-052c-43d1-8ddf-d2b07986c809', url: 'https://github.com/sravanth-12/JenkinsTF.git'
           }
        }
        stage('terraform Init') {
            steps{
                sh 'terraform init'
            }
        }
        stage('terraform apply') {
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
