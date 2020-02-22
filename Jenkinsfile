pipeline{
	agent any
	stages{
		stage ('Build'){
			steps{
				sh 'echo "Hellow World"'
				sh '''
					echo "Multiline shell "steps works too"
					ls -lah
				'''
			}
		}
	}
}
