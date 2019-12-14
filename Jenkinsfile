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
                branch 'when-condition-ci-cd'
            } 
            steps {
                withMaven(maven : 'LocalMaven') 
                {   
                    sh 'mvn compile' 
                } 
              
                  }


    }      
  }
}
