pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'This is Dev stage'
      }
    }

    stage('Q/A') {
      steps {
        echo 'this is qa'
      }
    }

    stage('build') {
      steps {
        echo 'this is build stage'
      }
    }

    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            echo 'this is uat'
          }
        }

        stage('deploy') {
          steps {
            echo 'this is deploy'
          }
        }

        stage('operate') {
          steps {
            echo 'this is operate stage'
          }
        }

      }
    }

  }
}