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
