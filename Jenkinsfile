pipeline {
    agent any
    stages {
        stage ('Upload to AWS') {
            steps {
                withAWS(region:’us-east-2’,credentials:’aws-static’){
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’udacity-jenkins06-09-2020’)
                }
                sh '''
                    echo "Multiline shell steps work too"
                    ls -lah     
                   '''
                   
                  }
               }
           }
     }
