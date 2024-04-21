pipeline {
    agent any 

    stages {
        stage('build') {
            steps {
              echo 'hello'
            }
        }

    }


        post {
            success {
                  emailext(to: 'marslandevops@gmail.com' , body: '$DEFAULT_CONTENT' , subject:'$DEFAULT_SUBJECT')
            }
        }
}

