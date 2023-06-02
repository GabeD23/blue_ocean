pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Print Test'
          }
        }

        stage('Parallel') {
          steps {
            echo 'Parallel'
          }
        }

      }
    }

    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Cleanup') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        echo 'Cleanup'
      }
    }

  }
}