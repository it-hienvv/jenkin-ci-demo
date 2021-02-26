pipeline {
    agent any
    stages {
        stage('build android') {
            tools {
                jdk 'JDK 8'
                nodejs 'NodeJs10'
            }
            steps {
                sh 'java -version'
                echo 'executing yarn ...'
                sh 'yarn'
                echo 'bundle install ...'
                dir('android') {
                    sh 'pwd'
                    sh 'bundle install --path vendor/bundle'
                    echo 'fast lane run ...'
                    sh 'bundle exec fastlane run_all'
                }
            }
        }
        
        stage('build ios') {
            tools {
                jdk 'JDK 8'
                nodejs 'NodeJs10'
            }
            steps {
                sh 'java -version'
                echo 'executing yarn ...'
                sh 'yarn'
                echo 'bundle install ...'
                dir('ios') {
                    sh 'pwd'
                    echo 'Pod file ...'
                    sh 'pod install --repo-update'
                    sh 'bundle install --path vendor/bundle'
                    echo 'fast lane run ...'
                    sh 'bundle exec fastlane config_app'
                }
            }
        }
    }
}
