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

}























