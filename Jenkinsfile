pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent any
    
    stages {
     
        stage('build'){
             steps {
                echo 'build !'
            }
        }

        stage('Deployment production'){

            when {
                branch 'prod'
            }

            steps {

                echo ' deploy '
            }
        }
    }

}
