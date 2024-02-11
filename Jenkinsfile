pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins'
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

                env
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