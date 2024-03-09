pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
  
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                   
                    sh './output'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                
            }
        }
    }
    
    post {
        always {
            script {
                
                if (currentBuild.result == 'FAILURE') {
                    echo 'Pipeline failed'
                }
            }
        }
    }
}
