pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
		sh 'cd webapp && docker build -t ravi2krishna/lms .'
            }
        }

        stage('Push') {
            steps {
                echo 'Deploying......'
		sh 'docker push ravi2krishna/lms'
            }
        }
    }
}
