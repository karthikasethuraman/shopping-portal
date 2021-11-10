pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build job invoked'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'Test job invoked'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'Package job invoked'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}