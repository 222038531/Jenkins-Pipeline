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
					mail body: 'Unit test sucessfull',
						subject: 'Unit Test',
						to: 's222038631@gmail.com',
						attachments: '$WORKSPACE/build.log'

				}
			}
		}
	}
}
