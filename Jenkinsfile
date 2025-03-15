
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
                step {
                    sh 'echo $VAR1'         // prints 'foo'
                }
            step {
                echo 'building ...1'
            }    
            }
        } 

        
        stage ('test') {
            environment {
                VAR1 = 'test'
            }   
            steps {
                step {
                    sh 'echo $VAR1'         // prints 'test'
                }
                step {
                    echo 'testing...1'
                }
            }
        }
    }
}    
