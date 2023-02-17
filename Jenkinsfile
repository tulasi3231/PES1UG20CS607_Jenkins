pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				sh 'g++ -c PES1UG20CS607-2.cpp'
				sh 'g++ -o PES1UG20CS607-1 PES1UG20CS607-2.cpp'
				echo 'build stage successful'
			}
		}
		stage('Test'){
			steps{
				sh './PES1UG20CS607-1'
				echo 'Test stage executed successfully'
			}
		}
		stage('Deploy'){
			steps{
				echo 'Deployed Successfully'
			}
		}
	}
	post{
		failure{
			echo 'Pipeline Failed'
		}
	}
}
