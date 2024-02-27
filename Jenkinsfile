pipeline {
    agent any    
    stages {
        stage('Build') {
            steps {                
                bat 'npm install'
              
                
            }
        }
        stage('Deploy') {
            steps {
                parallel {
                    a: (
                        bat 'npm start'
                    )
                    b: (
                        bat 'npx json-server db.json'
                    )
                    
                }             
                   
            }
        }
    }
}