
pipeline {
    agent any
    tools {
        maven 'Maven399'  // Ensure this is configured in Jenkins Global Tool Configuration
        // dockerTool 'docker275'
    }
    environment {
        VAR1 = 'foo'
        VAR2 = 'bar'

        // DOCKER = '/Applications/Rancher Desktop.app/Contents/Resources/resources/darwin/bin/docker'
    }
    stages {
        stage('build') {
            // agent {docker 'ubuntu-alpine'}
            
            steps {
                echo 'building ...'                
                sh 'echo $VAR1'         // prints 'foo'
                sh 'mvn -version'
                sh 'mvn install'
                sh 'java --version'
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
                    sh '/usr/local/bin/docker build -t springboot-java-helloworld-nandhu .'
                }
            }
        }
    }
