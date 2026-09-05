pipeline{
    agent any
    environment{
        VERCEL_TOKEN = cerditional('vercel_token')
    }
    stages{
        stage('Install'){
            steps{
                bat 'npm install'
            }
        }
        stage('Testing'){
            steps{
                echo 'skipping the test'
            }
        }
        stage('Build'){
            steps{
                bat 'npm run build'
            }
        }
        stage('deploy'){
            steps{
                bat 'vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}