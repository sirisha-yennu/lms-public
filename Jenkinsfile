pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'cd webapp && npm install'
                sh 'cd webapp && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
		sh 'sudo scp -r webapp/dist ubuntu@172.31.14.36:/var/www/html/'
            }
        }
    }
}
