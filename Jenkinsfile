pipeline {
	agent any

	tools {
		nodejs 'NodeJs-25'
	}

	environment {
        NODE_ENV = 'development'
      }


	stages {
		stage('Install') {
			steps {
				sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
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