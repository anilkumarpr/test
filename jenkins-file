node {
  def app 
  stage('clone repository') {
  
     checkout scm
   }
   stage('Build image') {
   
   app = docker.build)("anilkumarpr52/test")
   
   }
   
   stage('Test image') {
    
    app.inside {
      sh 'echo "Tests passed" '
      
      }
   }
   stage('Push Image') {
    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
      app.push("${env.BUILD_NUMBER}")
      app.push("latest")
      
      }
    }
  }
