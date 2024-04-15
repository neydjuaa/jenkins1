pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent any

    parameters {
        booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'production')
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
                equals expected: true, actual: params.DEPLOY_TO
              }
            }

            steps {

                echo ' deploy '
            }
        }
    }

}
