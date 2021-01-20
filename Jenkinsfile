pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'started'
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
        echo 'deployed'
      }
    }

  }
  environment {
    JAVA_LOC = 'C:/Program'
  }
}