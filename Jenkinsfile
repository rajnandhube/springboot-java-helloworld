pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                step {
                    echo 'Building..'
            }
                step {
                    sh "mvn install"
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
}
}

