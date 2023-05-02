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
					mail attachLog: true, 
					to: "s222038631@gmail.com",
					subject: "Unit Test",
					body: "Unit test was successful"
				}
			}
		}
	}
}
