pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building & Deploy VM'
                sh 'cd webapp && npm install'
                sh 'cd webapp && npm run build'
		sh 'cat dist/index.html'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
		sh 'cat dist/index.html'
		//sh 'cat /home/ubuntu/dist/index.html'
		//sh 'scp -r webapp/dist ubuntu@172.31.14.36:/home/ubuntu/dist'
            }
        }
    }
}
