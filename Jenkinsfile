pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
		sh 'docker build -t ravi2krishna/lms -f webapps/Dockerfile'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
            }
        }
    }
}
