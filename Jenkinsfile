pipeline{
    agent any
    environment{
        VERCEL_TOKEN = credentials('vercel_token')
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
                bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN% --name=Ali'

            }
        }
    }
}