pipeline {
  agent any
  stages {
    stage("Test") {
      agent {
          docker {
            image 'python:3.8-slim-buster'
          }
      }
      steps {
        sh "pip install poetry"
        sh "poetry install"
        sh "poetry run pytest"
      }
    }
  }
}


