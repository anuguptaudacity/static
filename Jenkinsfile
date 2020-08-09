pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                  withAWS(region:'us-east-2') {
                        sh 'echo "hello"'
}
               sh 'echo "hello world"'
               sh '''
		echo "multiline shell steps works too"
		ls -1ah
              '''
            }
        }
    }
}
