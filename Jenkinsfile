pipeline{
    agent { label java17 }
    triggers { pollSCM '* * * * *' }
    tools {
        maven ( maven3.9 )
        jdk ( java17)
    }
    stages {
        stage ( git ) {
            steps {
                git url 'https://github.com/jagadeesh9666/spring-petclinic-1.git',
                    branch 'main'
            }
        stage ( mvn package ) {
            steps {
                sh: 'mvn package'
            }
        }
    }

}