pipeline {
  agent {
    node {
      label 'ansible'
    }

  }
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
      steps {
        readFile 'install_Apache.yml'
      }
    }

  }
}