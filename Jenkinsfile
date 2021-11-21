pipeline{
	agent any
	stages{
		stage("Run Test"){
			steps{
				sh 'echo "Started...!" '
				sh 'docker-compose up'
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}

}
