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

                    }

                stages {
                    stage('Build') {
                        steps {
                            echo "Construire pour ${PLATFORM} " 
                        }
                    }
                    stage('Test') {
                        steps {
                            echo "Test pour ${PLATFORM} "
                        }
                    }

                    stage('Deploy'){
                        steps{
                            echo "Deploiement sur ${PLATFORM}"
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
