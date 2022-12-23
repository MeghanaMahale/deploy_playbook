pipeline {
  agent none
  stages {
    stage('Check for files in workspace') {
      agent {
        node {
          label 'ansible'
        }

      }
      steps {
        findFiles()
      }
    }

    stage('Check for Python') {
      agent {
        node {
          label 'ansible'
        }

      }
      steps {
        readFile 'test.yml'
      }
    }

  }
}