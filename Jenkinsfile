pipeline {
	agent any

	tools {
		nodejs 'NodeJs-25'
	}

	environment {
        NODE_ENV = 'development'
      }

	stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
    post {
        success {
          echo 'Build succeeded'
        }
        failure {
          echo 'Build failed'
        }
      }

}