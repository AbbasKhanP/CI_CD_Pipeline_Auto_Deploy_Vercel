pipeline{
    agent any
    environment{
        VERCEL_TOKEN = crecentrails ('vercel_token')
    }
    stages{
        stage{
            steps('Install'){
                bat 'npm install'
            }
        }
        stage{
            steps('Testing'){
                echo 'skipping the testing'
            }
        }
        stage{
            steps('Building'){
                bat 'npm run build'
            }
        }
        stage{
            steps('Deploy'){
                bat 'npm vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}