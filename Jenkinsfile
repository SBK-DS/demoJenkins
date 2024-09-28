pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo "this is build step"
pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This is a test stage'
          }
        }

        stage('Test Parallel') {
          steps {
            echo 'this is parallel job'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'this is deploy'
        sleep 10
      }
    }

  }
}