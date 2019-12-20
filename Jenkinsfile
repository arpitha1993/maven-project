pipeline {
	agent any
	stagesn{
		stage('one') {
			steps {
			      echo 'hi this is arpitha'
			      }
				}
		stage('two') {
			steps {
			      input('do yu want to proceed?')
			}
				}
		stage('three') {
			when {
				not {
			              branch "master"
			      }
				}
			steps {
				echo "hello"
			}
	}
		stage ('four') {
			parallel {
				stage('unit test') {
					steps {
						echo "running the unit test..."
					}
				}
				stage('integration test') {
					agent {
						docker {
							reuseNode false
							image 'ubuntu'
						}
					}
					steps {
						echo 'running the integration test..'
					}
				}
			}
		}
	}
}
