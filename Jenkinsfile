pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo"Maven Building Application..."
			}
		}
		stage('Test'){
			steps{
				echo "Unit tests"
			}
			post{
				success{
					emailext body: 'Unit test successful', compressLog: true, subject: 'Unit Test', to: 's222038631@gmail.com'
				}
			}
		}
	}
}
