pipeline{
    agent any
    environment{
        VERCEL_TOKEN = credentials ('vercel_token')
    }
    stages{
        stage('Install'){
            steps{
                bat 'npm install'
            }
        }
        stage('Testing'){
            steps{
                echo 'skipping the testing'
            }
        }
        stage('Building'){
            steps{
                bat 'npm run build'
            }
        }
        stage('Deploy'){
            steps{
                bat 'npm vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}