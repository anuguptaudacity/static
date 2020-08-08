pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               sh 'echo "hello world"'
               sh '''
	echo "multiline shell steps works too"
	ls –1ah
              '''
            }
        }
    }
}
