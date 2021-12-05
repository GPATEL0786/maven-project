pipeline
{
 agent any{
stages
{ 
 
 stage('scm checkout')
 {

 steps { git branch: 'master', url: 'https://github.com/GPATEL0786/maven-project.git' } }


  stage ('create package') { 
 steps {
    sh 'mvn package'
    }
 }

}
}
}
