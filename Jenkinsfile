pipeline {
    // pipeline est éxécuté sur n'importe quel agent disponible
    agent {
        docker {
            image 'node:21-alpine'
        }
    }

    stages {
     
        stage('build'){
            steps {
             sh 'npm -v'
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










