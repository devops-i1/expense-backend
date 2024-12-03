pipeline {
  agent {
    node {
      label 'ci-server'
    }
  }

  stages {
    stage('Lint Code') {
      when {
        allOf {
          not { buildingTag() }
          branch 'main'
        }
      }
      steps {
        echo 'Lint Code'
      }
    }

    stage('Run Unit Tests') {
      when { not { buildingTag() } }
      steps {
        echo 'Run Unit Tests'
      }
    }

    stage('Run Integration tests') {
      when { not { buildingTag() } }
      steps {
        echo 'Run Integration tests'
      }
    }

    stage('Sonar Scan code review') {
      when {
        allOf {
          not { buildingTag() }
          branch 'main'
        }
      }
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