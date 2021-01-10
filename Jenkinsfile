pipeline
{
agent any
stages
{
stage('SCM CHECKOUT')
{steps
{git 'https://github.com/GPATEL0786/maven-project'

}
}
stage('please compile code')
    {steps
     {withMaven(jdk: 'Gaurav-Home', maven: 'Gaurav-Maven') {
    sh 'mvn compile'
}
       
     }
    
    }
    stage('please test code')
    {steps
     {withMaven(jdk: 'Gaurav-Home', maven: 'Gaurav-Maven') {
    sh 'mvn test'
}
       
     }
    
    }
stage('please build code')
    {steps
     {withMaven(jdk: 'Gaurav-Home', maven: 'Gaurav-Maven') {
    sh 'mvn package'
}
       
     }
    
    }
    stage('deploy on tomcat')
{steps
{
sshagent(['d1dcd31f-8d1d-48b3-bf7f-6ea5a34d095a']) {
    sh 'scp -o StrictHostKeyChecking=no */target/webapp.war ec2-user@172.31.2.73:var/lib/tomcat/webapps'
}
}
}








}
}
