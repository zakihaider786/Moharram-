pipeline {
  agent any
  stages {
    stage('Deploy to Desktop') {
      steps {
        bat(script: 'xcopy /E /Y "%WORKSPACE%\\*" "C:\\Users\\CT-Zaki\\Desktop\\moharram"', returnStatus: true, returnStdout: true)
      }
    }

  }
  environment {
    DEPLOY_DIR = 'C:\\Users\\CT-Zaki\\Desktop\\moharram'
  }
}