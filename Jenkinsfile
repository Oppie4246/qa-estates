pipeline {
    agent any    
    stages {
        stage('Build') {
            steps {                
                bat 'npm install'
                bat 'npm start'
                bat 'npx json-server db.json'
            }
        }
        stage('Deploy') {
            steps {                
                bat 'npm run preview'       
            }
        }
    }
}