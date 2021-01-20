pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'started'
        bat 'echo "welcome"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'second step'
          }
        }

        stage('paralleltest') {
          steps {
            echo 'parallel testing happened'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        bat 'echo "deployed"'
      }
    }

  }
  environment {
    JAVA_LOC = 'C:/Program'
  }
}