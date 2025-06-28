pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Clean Old Files') {
            steps {
                bat '''
                rmdir /S /Q "C:\\Users\\CT-Zaki\\Desktop\\moharram"
                mkdir "C:\\Users\\CT-Zaki\\Desktop\\moharram"
                '''
            }
        }

        stage('Deploy Files') {
            steps {
                bat '''
                xcopy /E /Y "%WORKSPACE%\\*" "C:\\Users\\CT-Zaki\\Desktop\\moharram"
                '''
            }
        }

        stage('Done') {
            steps {
                echo '✅ Deployment Successful to Desktop!'
            }
        }
    }
}
