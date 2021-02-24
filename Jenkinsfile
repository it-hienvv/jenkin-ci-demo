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
               	echo 'executing yarn ...'
                sh 'yarn'
                echo 'bundle install ...'
		dir('android') {
      		   sh "pwd"
                }
		sh 'cd android'
	        sh 'bundle install --path vendor/bundle'
		echo 'fast lane run ...'
                sh 'bundle exec fastlane run_all'
            }
        }
    }
}
