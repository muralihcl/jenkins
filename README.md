# Jenkinsfile - making the easy things easy

This repository is created to demonstrate usage of Jenkinsfile to pass the instructions to the Jenkins Pipeline


# Example

This example runs a very simple set of build processes. This would work with pipeline-as-code and branch source.

```
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
```
