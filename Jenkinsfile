pipeline {
    agent any
    stages {
      stage('Lint HTML') {
        steps {
          bat 'tidy -q -e *.html'
        }
      }
      stage ('Upload to AWS'){
        steps {
          withAWS(region:'us-east-1',credentials:'jenkins') {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'c3pipelines')
          }
        }
      }
    }
}
