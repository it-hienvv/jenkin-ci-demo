pipeline {
    agent any  
    stages {
        stage('build') {
            steps {
                echo 'executing yarn ...'
                GIT_COMMIT_EMAIL = sh (
                    script: 'which fastlane',
                    returnStdout: true
                ).trim()
                echo "Git committer email: ${GIT_COMMIT_EMAIL}"
            }
        }
    }
}
