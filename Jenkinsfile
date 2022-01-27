pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    
    post
    {
        always
        {
            slackSend channel: 'development', message: "please find status of pipeline-${currentBuild.currentResult} ${env.JOB_NAME} ${env.BUILD_NUMBER} ${env.BUILD_URL}"
        }
    }
}
