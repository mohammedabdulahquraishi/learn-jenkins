pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = 'Hello Jenkins, I am Abdulah'
    }
    parameters {
        string (name:'PERSON', defaultValue:'Mr.Jenkins', description:'who are you')
        booleanParam(name: 'TOGGLE',defaultValue:'toggle', description:'toggle' )
        choice(name: 'CHOICE', defaultValue:'CHOICE', description:'give your choice here')

    }
    stages {
        stage('build') {
            steps {
                echo "Hello world!"
                echo 'hello ${params.PERSON}'
                echo '$(params.TOGGLE)'
                echo '${params.CHOICE}'

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
                echo 'deploying jenkins ...............
                $GREETING'
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