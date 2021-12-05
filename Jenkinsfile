pipeline
{
agent 
 { label 'akua' }
  
stages
{ 
 
 stage('scm checkout')
 { steps { git branch: 'master', url: 'https://github.com/prakashk0301/maven-project.git' } }


 stage ('run unit test framework')
 { steps { withMaven(jdk: 'JAVA_HOME', maven: 'M2_HOME') 
   {
    sh 'mvn test'
    }
 } }

  stage ('create package')
 { steps { withMaven(jdk: 'JAVA_HOME', maven: 'M2_HOME') 
   {
    sh 'mvn package'
    }
 } }


}
}

