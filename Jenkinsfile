pipeline {
  agent any
  stages {
    stage('Clone repo locally') {
      steps {
        sh '''echo "Start cloning of git repo"
'''
      }
    }

    stage('Completed') {
      steps {
        sh 'echo "Completed"'
        emailext(subject: '"[Jenkins Build Server] Status Update- ${currentBuild.currentResult}: Job- ${env.JOB_NAME}"', body: '"${currentBuild.currentResult}: Job Name - ${env.JOB_NAME} Build No - ${env.BUILD_NUMBER}\\n More info can be found at: ${env.BUILD_URL}"', from: 'peter.aw@outlook.com', to: 'peter.aw@outlook.com')
      }
    }

  }
}