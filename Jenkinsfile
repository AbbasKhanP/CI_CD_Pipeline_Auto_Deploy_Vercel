pipeline{
    agent any
    environment{
        VERCEL_TOKEN=cerdical('vercel_token')
    }
    stages{
        stage('Install'){
            steps{
                bat 'npm install'
            }
        }
        stage('Test'){
            steps{
                echo 'skipping the test'
            }
        }
        stage('Build'){
            steps{
                bat 'npx run build'
            }
        }
        stage('Deploy'){
            steps{
                bat 'npx vercel --prod --yes --vercel "%VERCEL_TOKEN%"'
            }
        }
    }
}