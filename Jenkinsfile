pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World from reservations'
            }
		}
		stage('Checkout code') {
			steps {
			   ws("/conf-docker/backend-resa/backend-api-resa") {
				  checkout scm
			   }
			}
		}
		stage('recompose docker container') {
			steps {
			    ws("/conf-docker/backend-resa") {
				     sh('date > lastUpdate.txt')
				}
			}
		}
    }
}
