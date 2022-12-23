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
      parallel {
        stage('Read file test.yml') {
          agent {
            node {
              label 'ansible'
            }

          }
          steps {
            readFile 'test.yml'
          }
        }

        stage('Check for Python') {
          agent {
            node {
              label 'ansible'
            }

          }
          steps {
            readYaml(file: 'test.yml', text: ' Check for Python')
          }
        }

      }
    }

  }
}