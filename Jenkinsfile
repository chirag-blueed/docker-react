pipeline {
    agent any
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
        disableConcurrentBuilds()
    }
    stages {
        stage('Hello') {
            steps {
                echo 'hello React'
            }
        }
        stage('cat README') {
            when {
                branch "test-1*"
            }	
            steps {
                sh '''
                    cat README.md
                '''
            }
        }
	
    }
}
