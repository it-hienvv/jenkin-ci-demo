pipeline {
    agent any  
    stages {
        stage ("first") {
            tools {
                jdk "jdk-1.8.101"
            }
            steps {
                sh 'java -version'
            }
        }
        stage('build') {
            steps {
                echo 'executing yarn ...'
                sh 'cd android && bundle install && bundle exec fastlane build_rl'
            }
        }
    }
}
