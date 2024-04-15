pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent any

    environment {
        DEPLOY_TO = 'prod'
    }
    
    stages {
     
        stage('build'){
             steps {
                echo 'build !'
            }
        }

        stage('Deployment production'){

            when {
              allOf {
                branch 'main'
                environment name: 'DEPLOY_TO', value: 'prod'
              }
            }

            steps {

                echo ' deploy '
            }
        }
    }

}
