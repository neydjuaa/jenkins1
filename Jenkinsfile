pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent any

    stages {


        stage('Build and test') {

                matrix {

                    axes {

                        axis {
                            name 'PLATFORM'
                            values 'linux','macos','windows'
                        }

                        axis {
                            name 'BROWSER'
                            values 'firefox','chrome','safari'
                        }
                    }

                stages {
                    stage('Build') {
                        steps {
                            echo "Construire pour ${PLATFORM} - ${BROWSER}" 
                        }
                    }
                    stage('Test') {
                        steps {
                            echo "Test pour ${PLATFORM} - ${BROWSER}" 
                        }
                    }
                }


          }



        }


     
        stage('Deployment production'){
             steps {
                echo 'deploy !'
            }
        }
       
    }

}
