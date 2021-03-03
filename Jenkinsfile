pipeline {
  agent any
  stages {
    stage('SSH') {
      steps {
        sh '''sshagent (credentials: [\'ssh-logisoft\']) {
                    sh \'\'\'
                        ssh -o StrictHostKeyChecking=no $SSH_INFO "
                        cd /var/dev/web/laradock
docker-compose restart workspace
                        "
                    \'\'\'
                }'''
        }
      }

    }
    environment {
      SSH_INFO = 'logisoft@wms247go.com'
    }
  }