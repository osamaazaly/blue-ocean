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
        echo 'deployment completed'
      }
    }

  }
}