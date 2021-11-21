pipeline{
	agent any
	stages{
		stage("Run Test"){
			steps{
				ls -al
				docker-compose up
			}
		}
		stage("Bring Grid Down"){
			steps{
				sh "docker-compose down"
			}
		}
	}

}
