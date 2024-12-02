pipeline {
  agent {
    node {
      label 'ci-server'
    }
  }

  stages {

    stage('Lint Code') {
      steps {
        echo 'Lint Code'
      }
    }

    stage('Run Unit Tests') {
      steps {
        echo 'Run Unit Tests'
      }
    }

    stage('Run Integration tests') {
      steps {
        echo 'Run Integration tests'
      }
    }

    stage('Sonar Scan') {
      steps {
        echo 'Sonar Scan'
      }
    }

    stage('Release Software') {
      steps {
        echo 'Release Software'
      }
    }
  }

}