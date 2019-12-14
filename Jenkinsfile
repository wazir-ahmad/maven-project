pipeline {
    agent any
    stages 
    {       
        stage ('SCM Checkout') {
          git url: 'https://github.com/prakashk0301/maven-project'
         }  
    }
    {
        stage ('Compile Stage') {
            when {
                branch "ci-cd-pipeline"
            } 
            steps {
                withMaven(maven : 'LocalMVN') 
                {   
                    sh 'mvn compile' 
                }            
            }
    }      
  }
    { stage ('package') {
        when {
                branch "master"
            } 
        steps {
                withMaven(maven : 'LocalMVN') 
                {   
                    sh 'echo hello' 
                }            
            }
    }
    }
}
