
pipeline {
    agent any
    environment {
        VAR1 = 'foo'
        VAR2 = 'bar'
    }
    stages {
        stage('build') {
            // agent {docker 'ubuntu-alpine'}
            
            steps {
                sh 'echo $VAR1'         // prints 'foo'
                echo 'building ...1'
            }
        } 

        
        stage('test') {
            environment {
                VAR1 = 'test'
            }   
            steps {
                    sh 'echo $VAR1'         // prints 'test'
                    echo 'testing...1'
                }
            }
        }
    }
