pipeline {
	agent any
	environment {
		NEW_VERSION = '1.0.0'
		ADMIN_CREDENTIALS = credentials('admin_user_credentials')
	}
	stages {
		stage("build") {
			steps {
				echo 'building the applicaiton...'
				echo "building version ${NEW_VERSION}"
			}
		}
		stage("test") {
			steps {
				echo 'testing the applicaiton...'
			}
		}
		stage("deploy") {
			steps {
				echo 'deploying the applicaiton...'
				echo "deploying with ${ADMIN_CREDENTIALS}"
				sh 'printf ${ADMIN_CREDENTIALS}'
			}
		}
	}
}
