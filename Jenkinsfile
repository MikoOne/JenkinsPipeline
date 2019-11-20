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
            sh 'sh deploy.sh'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Test'
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
  environment {
    KEY1 = 'VALUE1'
    KEY2 = 'VALUE2'
  }
}