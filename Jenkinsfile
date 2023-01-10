pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
		sh 'cd webapps && docker build -t ravi2krishna/lms .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
            }
        }
    }
}
