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

        stage('Deploy K8S') {
            steps {
                echo 'Deploy On Cluster'
		//sh 'docker container rm -f c1'
                //sh 'docker container run -dt --name c1 -p 80:80 ravi2krishna/lms'
		sh 'kubectl get pod'
            }
        }	

}
}
