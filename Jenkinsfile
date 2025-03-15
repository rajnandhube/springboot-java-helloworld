
pipeline {
    agent any
    tools {
        maven 'Maven399'
    }
    environment {
        VAR1 = 'foo'
        VAR2 = 'bar'
    }
    stages {
        stage('build') {
            // agent {docker 'ubuntu-alpine'}
            
            steps {
                echo 'building ...'                
                sh 'echo $VAR1'         // prints 'foo'
                sh 'mvn -version'
                sh 'pwd'
                sh 'ls -latr'
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
