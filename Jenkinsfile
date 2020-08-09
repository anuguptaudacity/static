pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
                  echo "Multiline shell steps works too"
                  ls -1ah
               '''
      }
    }
        stage('Upload to AWS') {
        steps {
                 withAWS(region:'us-east-2',credentials:'aws-static1') {
                        def identity=awsIdentity();
                        sh 'echo "Uploading content with AWS creds"'
                        s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html',  bucket:'anu-udacity-project3') 
                    }
                 }
          }
           
  }
}


