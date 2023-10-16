node {
     stage('Clone repository') {
         checkout scm
     }
     stage('Build image') {
         app = docker.build("jeeunlee/flask-example")
     }
     stage('docker-push'){
            steps{
                echo 'Push Docker'
                script {
                    docker.withRegistry('', registryCredential){
                        dockerImage.push("1.0")
                    }
                }
                
            }
        }
      
}
 
