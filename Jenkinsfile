
pipeline {
    agent any
    tools {
        maven 'Maven399'
        docker 'docker275'
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
                sh 'mvn install'
            }
        } 

        
        stage('Build Docker Image') {
            environment {
                VAR1 = 'test'
            }   
            steps {
                    echo 'Docker image is building'
                    sh 'echo $VAR1'         // prints 'test'
                    sh 'docker -v'
                    sh 'docker build -t springboot-java-helloworld-nandhu .'
                }
            }
        }
    }
