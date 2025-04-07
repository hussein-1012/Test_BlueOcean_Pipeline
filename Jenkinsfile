pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed.'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test Completed'
          }
        }

        stage('Test2') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are You Sure to Deploy?', ok: 'Yes, I am sure.')
        echo 'Deploy Completed.'
      }
    }

  }
}