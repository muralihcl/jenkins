pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'mkdir some_directory' 
            }
        }
        stage('Test'){
            steps {
                sh 'cp /etc/*release some_directory'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls some_directory; cat some_directory/*release' 
            }
        }
    }
}
