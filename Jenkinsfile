pipeline {
    agent any  
    stages {
        stage('build') {
            steps {
                echo 'executing yarn ...'
                sh 'cd android && bundle install && bundle exec fastlane build_rl'
            }
        }
    }
}
