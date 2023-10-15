node {
     stage('Clone repository') {
         checkout scm
     }
     stage('Build image') {
         app = docker.build("jung-in-feb/flask-example")
     }
     stage('Push image') {  
         docker.withRegistry('https://registry.hub.docker.com/jeeunlee/', 'docker-hub') {
             app.push("${env.BUILD_NUMBER}")
             app.push("latest")
         }
     }
}
stage('Build image') {
  app = docker.build("jung-in-feb/flask-example")
}

stage('Push image') {
  docker.withRegistry('https://registry.hub.docker.com/jeeunlee/', 'docker-hub') 
  {
     app.push("${env.BUILD_NUMBER}")
     app.push("latest")
  }
} 

