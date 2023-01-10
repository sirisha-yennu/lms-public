pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building & Deploy VM'
		sh 'docker container ls'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
            }
        }
    }
}
