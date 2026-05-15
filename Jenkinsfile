pipeline {
  agent any

  stages {
    stage('Checkout Info') {
      steps {
        echo '✅ Jenkins is running this pipeline'
        echo "Branch: ${env.BRANCH_NAME}"
        echo "Workspace: ${env.WORKSPACE}"
        sh 'ls -la'
      }
    }

    stage('Dummy Build') {
      steps {
        echo '🔧 Simulating build...'
        sh 'sleep 5'
        echo 'Build completed'
      }
    }

    stage('Dummy Test') {
      steps {
        echo '🧪 Simulating tests...'
        sh 'sleep 3'
        echo 'All tests passed'
      }
    }
  }

  post {
    success {
      echo '🎉 Pipeline Success!'
    }
    failure {
      echo '❌ Pipeline Failed!'
    }
  }
}
