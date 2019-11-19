pipeline {
  agent {
    node {
      label 'MacPro'
    }

  }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'build'
            sh 'sh build.sh'
          }
        }

        stage('analyse') {
          steps {
            echo 'analyse'
          }
        }

      }
    }

    stage('deyloy') {
      parallel {
        stage('deyloy') {
          steps {
            echo 'deploy'
          }
        }

        stage('upload_product') {
          steps {
            echo 'upload'
          }
        }

        stage('test') {
          steps {
            echo 'test'
          }
        }

      }
    }

  }
  environment {
    KEY1 = 'VALUE1'
    KEY2 = 'VALUE2'
  }
}