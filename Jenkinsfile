pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
		sh 'cd webapp && docker build -t ravi2krishna/lms .'
            }
        }


 	stage('Push image') {
            steps {
        withDockerRegistry([ credentialsId: "docker", url: "" ]) {
        sh 'docker push ravi2krishna/lms'
        }
	}

    }
}
}
