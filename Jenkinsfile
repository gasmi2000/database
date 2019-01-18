
pipeline {
    agent any
    
    /*agent {  //dockerfile true }
    docker { image 'database:1.2' }
    }
    */

   
/*   okk
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
    */
    
  /*  agent {
    dockerfile {
        filename '.'
       // dir 'build'
       // label 'my-defined-label'
        registryUrl 'http://127.0.0.1:2375'
       // registryCredentialsId 'myPredefinedCredentialsInJenkins'
    }
}*/
   /* docker {
    //image "image name"
    registryUrl "http://127.0.0.1:2375"
    //registryCredentialsId "credsId"
  }*/
        
      
    stages {
      
        stage('build and deploy') {
      steps {
        /*
         * Multiline strings can be used for larger scripts. It is also possible to put scripts in your shared library
         * and load them with 'libaryResource'
         */
        sh """
          docker build -t database .
          docker tag database registry:5000/database
          docker push registry:5000/database
        """
      }
        }
        
        
          
        stage('Test') {
            steps {
                echo 'hello gasmi'
               
            }
            
        }
    }
}
