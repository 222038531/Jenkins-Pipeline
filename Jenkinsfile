pipeline {
	agent any
	stages{
		stage('Build'){
			steps{
				echo "Maven building application..."
			}
		}
		stage('Test'){
			steps{
				echo "Unit tests"
			}
		}
		stage('Code Analysis'){
			steps{
                echo "Starting Static Code Analysis Plug-in..."
                echo "SUCCESSFUL"
			}
		}
		stage('Security Scan'){
			steps{
                echo "Synk Security Scanner Scanning..."
                ehco "SUCESSFUL"
			}
		}
        stage{
            steps{
                echo "Deploying application to AWS staging server"

                }
            }
		stage('Integration Test'){
			steps{
		        echo "Integration testing..."
                echo "SUCESSFULL"
			}
		}
		stage('Deploy to Production'){
			steps{
                echo "Deploying application to AWS production server"
		}
	}
}

