pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building & Deploy VM'
		sh 'cd webapp && rm -rf dist'
                sh 'cd webapp && npm run build'
		sh 'scp -r webapp/dist ubuntu@172.31.14.36:/home/ubuntu/dist'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
		sh 'cd webapp && cat dist/index.html'
		//sh 'cat /home/ubuntu/dist/index.html'
		//sh 'scp -r webapp/dist ubuntu@172.31.14.36:/home/ubuntu/dist'
            }
        }
    }
}
