pipeline {
    agent any  
    stages {
        stage('build') {
            tools {
                jdk "JDK 8"
                nodejs "NodeJs10"
            }
            steps {
                sh 'java -version'
                sh 'npm i'
                echo 'executing yarn ...'
                sh 'cd android && bundle install && bundle exec fastlane run_all'
            }
        }
    }
}
