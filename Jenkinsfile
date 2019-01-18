
pipeline {
   /* agent { dockerfile true }
    docker { image 'database' }
          */
    
    environment {
    registry = "registry:5000/database"
   // registryCredential = 'dockerhub'
  }
   
   
    agent {
        
    dockerfile {
        filename 'Dockerfile'
        //dir 'build'
        //label 'my-defined-label'
        additionalBuildArgs  '-t database:1.0'
        //args '-v /tmp:/tmp'
       registryUrl 'http://registry:5000'
    }
        
    }
    
   
  
      
    stages {
       
       stage('Taggg') {
          
         
          
      steps {
         
          script {
        //  docker.build registry + ":$BUILD_NUMBER"
             sh "docker tag database:1.0 registry:5000/database:1.0"
        }
         
         
        //sh "docker tag database:1.0 registry:5000/database:1.0"
      }
       }
          
          
        stage('Test') {
            steps {
                echo 'hello gasmi'
               
            }
            
        }
    }
}
