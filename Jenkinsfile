pipeline{
	agent any
	stages {
		stage('Start Grid'){
			steps {
				bat 'docker-compose up -d hub chrome firefox'
				bat 'docker images'
			}
		}
		stage('Run Test'){
			steps{
				bat 'docker-compose up testngFirst testngSecond'
			}
		}
		stage('Stop Grid'){
			steps{
				bat 'docker-compose down'
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
		}
	}

}
