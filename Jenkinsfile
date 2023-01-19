pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building & Deploy VM'
		sh 'cd webapp && rm -rf dist'
		sh 'cd webapp && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
 		sh 'scp -r webapp/dist ubuntu@100.26.166.255:/home/ubuntu/'
            }
        }
    }
}
