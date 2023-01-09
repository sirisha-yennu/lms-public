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
		sh 'cat /home/ubuntu/dist/index.html'
		sh 'scp -r webapp/dist ubuntu@172.31.14.36:/home/ubuntu/dist'
            }
        }
    }
}
