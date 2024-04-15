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
            input {
                message 'Voulez-vous déployez en production ? '
                ok 'deployer!'
                submitter 'admin, devops'
                submitParameter 'USER_SUBMIT'
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'La version déployée')
                }
            }
            steps {
                echo "User: ${USER_SUBMIT}"
                echo "Version: ${VERSION}"
                echo ' deploy '
            }
        }



      

    }

}
