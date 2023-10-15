node {
     stage('Clone repository') {
         checkout scm
     }
     stage('Build image') {
         app = docker.build("jung-in-feb/flask-example")
     }
      
}
 
