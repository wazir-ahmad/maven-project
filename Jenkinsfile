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
stage ('maven test')
{ steps {
withMaven(jdk: 'LocalJDK', maven: 'LocalMVN') {
    sh 'mvn test'
}
}
}
}

{
stage ('build')
{ steps
{
withMaven(jdk: 'LocalJDK', maven: 'LocalMVN') {
    sh 'mvn clean package'
}
}
}

}
}



























