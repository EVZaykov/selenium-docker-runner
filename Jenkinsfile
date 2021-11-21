pipeline{
	agent any
	stages{
		stage("Run Test"){
			steps{
				echo 'ls -al'
				echo 'docker-compose up'
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}

}
