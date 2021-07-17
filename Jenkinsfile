pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build completed'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test '
          }
        }

        stage('test 1') {
          steps {
            echo 'running test 1'
          }
        }

      }
    }

    stage('depoy') {
      steps {
        input(message: 'Are you to deploy ?', ok: 'Yes, i am')
        echo 'Deployment completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build started'
      }
    }

  }
}