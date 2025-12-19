@Library('my-shared-lib') _

import org.devops.Utils

pipeline {
  agent any

  stages {
    stage('Init') {
      steps {
        script {
          def utils = new Utils(this)
          utils.printMessage("Pipeline started")
        }
      }
    }
    stage('Build') {
      steps {
        buildApp()
      }
    }
    stage('Docker') {
      steps {
        buildDocker("demo-app:latest")
      }
    }
  }
}
