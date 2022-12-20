pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withGradle()
      }
    }

    stage('TestUnitaire') {
      parallel {
        stage('TestUnitaire') {
          steps {
            sh '''gradlew task-name
'''
            sh 'gradlew task-name'
          }
        }

        stage('Integration') {
          steps {
            sh '''gradlew task-name
'''
          }
        }

        stage('Fonctionnel') {
          steps {
            sh '''gradlew task-name
'''
          }
        }

      }
    }

    stage('Deploiment') {
      steps {
        sh '''gradlew task-name
'''
      }
    }

  }
}