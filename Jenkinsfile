pipeline {
    agent any 

    tools {
       gradle 'gradle8.6' 
       nodejs 'node21'
    }

    stages {
        stage('build') {
            steps {
            
                sh 'gradle -v'
                sh 'node -v'

            }
        }
    }
}





