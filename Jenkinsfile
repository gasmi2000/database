
pipeline {
   /* agent { dockerfile true }
    docker { image 'database' }
          */
    
    agent {
        
    dockerfile {
        filename 'Dockerfile'
        //dir 'build'
        //label 'my-defined-label'
        additionalBuildArgs  '-t database:1.0'
        //args '-v /tmp:/tmp'
    }
        
    }
    
    stages {
        stage('Test') {
            steps {
                echo 'hello gasmi'
               
            }
            
        }
    }
}
