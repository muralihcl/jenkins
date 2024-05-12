pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'uname -a' 
            }
        }
        stage('Test'){
            steps {
                sh 'cat /etc/*release'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo published' 
            }
        }
    }
}
