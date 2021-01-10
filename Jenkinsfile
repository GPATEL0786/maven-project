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

}
stage('plesae compile code')
    {steps
     {withMaven(jdk: 'Gaurav-Home', maven: 'Gaurav-Maven')
    sh 'mvn compile'
}
    }


}
}
