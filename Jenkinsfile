pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent {
        docker {
            image 'node:21-alpine'
        }
    }
    

    


    stages {
     
        stage('build'){
        
            options {
                timestamps()
            }
            steps {
             sh 'npm -v'
             sh sleep 15
             echo 'hahah'
            }
        }

    }

    post {
        always {
          echo 'always'
        }
        success{
            echo 'success !'
        }
    }
}










