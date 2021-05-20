pipeline {
  agent {
    label 'NODEJS'
  }

  stages {
    stage('Prepare Artifacts') {
       steps {
       sh '''
         zip -r ../login.zip *
       '''
       }
    }
    stage('Upload Artifacts') {
        steps {
            sh '''
            curl -v -u admin:Omkar@123 --upload-file /home/ubuntu/workspace/login.zip http://172.31.4.7:8081/repository/login/login.zip
            '''
        }
    }
  }
}
