pipeline {
agent any

stages
{
stage('cloning code')
{
steps 
{git 'https://github.com/prakashk0301/maven-project'
}
}
}
  { 
stage ('build job')
  {
    steps {   
     withMaven(jdk: 'LocalJDK', maven: 'LocalMVN') {

      sh ' mvn install '
    }}}
}
  { 
    stage (' deploy to tomcat')
    {
      steps {
  
  sshagent(['tomcat']) {
    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.37.250:/var/lib/tomcat/webapps/'
  }}}
    
    
  }   
    
}
  
























