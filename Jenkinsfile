pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('build') {
            steps {
                echo 'Hello world!'
            }
        }
        stage('test') {
            steps {
                echo 'testing'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying jenkins ...............'
            }
        }
    }
}