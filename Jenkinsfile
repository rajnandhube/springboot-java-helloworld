pipeline {
	agent any
	stages {
		stage (Build) {
			steps {
				step {
					echo "Build is started"
				}
				step {
					sh "mvn install"
				}
			}
		}
		stage (test) {
			steps {
				step {
					echo "Testing"
				}
				step {
					echo "testing by nandhu"

				}
			}
		}

	}
}
