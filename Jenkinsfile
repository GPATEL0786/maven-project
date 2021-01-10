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
    stage('please package code')
    {steps
     {withMaven(jdk: 'Gaurav-Home', maven: 'Gaurav-Maven') {
    sh 'mvn package'
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








}
}
