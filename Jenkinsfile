pipeline {
  agent any
  stages {
    stage('move') {
      parallel {
        stage('move') {
          steps {
            echo 'moving'
          }
        }

        stage('move2') {
          steps {
            echo 'copying'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sleep 2
      }
    }

    stage('verify') {
      steps {
        sleep 2
      }
    }

    stage('notify') {
      steps {
        emailext(subject: 'done', body: 'done', from: 'jenkins')
      }
    }

  }
}