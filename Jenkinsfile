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

    stage('Sonar Scan code review') {
      steps {
        echo 'Sonar Scan'
      }
    }

    stage('Build Code') {
      when { buildingTag() }
      steps {
        echo 'Build Code'
      }
    }

    stage('Release Software') {
      when { buildingTag() }
      steps {
        echo 'Release Software'
      }
    }
  }

}