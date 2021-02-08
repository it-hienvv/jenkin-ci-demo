pipeline {
    agent any  
    stages {
        stage('build') {
            steps {
                echo 'executing yarn ...'
                sh 'cd android && bundle install'
                sh '~/.fastlane/bin/bundle/bin/fastlane build_rl'
            }
        }
    }
}
