pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins, I am Abdulah'
    }
    stages {
        stage('build') {
            steps {
                echo "Hello world!"

            }
        }
        stage('test') {
            steps {
                echo 'testing'
            }
        }
        stage('deploy') {
            steps {
                sh """ 
                echo 'deploying jenkins ...............'
                echo '$GREETING'
                """
            }
        }
    }
    post {
          failure{
               echo "This runs when pipeline is failed."
            }
          
          always {
            echo "This runs always"
          }
          success {
            echo "This runs if success"
          }
        }
        
                
            
}