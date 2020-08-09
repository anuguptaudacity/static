pipeline {
  agent any 
  stages {
stage('Lint HTML.'){
                  steps {
                        sh "tidy -q -e *.html"
                  }
            }
        stage('Upload to AWS') {
        steps {
                 withAWS(region:'us-east-2',credentials:'aws-key1') {
                       // sh 'echo "Uploading content with AWS creds"'
                        s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html',  bucket:'anu-udacity-project3') 
                        sh 'echo "Bucket Uploaded completed with AWS creds"'
                    }
                 }
          }
           
  }
}
