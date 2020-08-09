pipeline {
      agent any
      stages {
            stage('Upload to AWS.') {
                steps {
                    withAWS(region:'us-east-2',credentials:"aws-static") {
                        s3Upload(file:'index.html', bucket:'anu-udacity-project3', path:'index.html')
                    }

                    sh 'echo "Hello World"'
                    sh '''
                        echo "Multiline shell steps works too"
                        ls -1ah
                    '''
                  }

            }
        
      }
}
