pipeline {
  agent any
  stages {
    stage('SSH') {
      steps {
        sh '''ssh -o StrictHostKeyChecking=no $SSH_INFO -T << EOF
cd /var/dev/web/laradock
docker-compose restart workspace
EOF'''
      }
    }

  }
  environment {
    SSH_INFO = 'logisoft@wms247go.com'
  }
}