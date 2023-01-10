pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
		sh 'cd webapp && docker build -t ravi2krishna/lms .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
            }
        }
    }
}
