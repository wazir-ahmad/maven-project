pipeline {
    agent any
    stages 
    {       
        stage ('SCM Checkout') {
          git url: 'https://github.com/prakashk0301/maven-project', branch: 'master'
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
        steps {
                withMaven(maven : 'LocalMVN') 
                {   
                    sh 'echo hello' 
                }            
            }
    }
    }
}
