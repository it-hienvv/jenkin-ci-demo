pipeline {
    agent any  
    stages {
        stage('build') {
            tools {
                jdk "JDK 8"
            }
            steps {
                sh 'java -version'
            }
            steps {
                echo 'executing yarn ...'
                sh 'cd android && bundle install && bundle exec fastlane build_rl'
            }
        }
    }
}
