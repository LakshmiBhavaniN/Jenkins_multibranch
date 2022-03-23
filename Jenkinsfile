library identifier: 'mylibraryname@main',
    retriever: modernSCM([
      $class: 'GitSCMSource',
      credentialsId: 'git_credentials', remote: 'https://github.com/lakshmiKrishnaa/vars.git'
])

pipeline {
    agent any
    //  tools {
      //maven 'MAVEN_HOME'

    //}
    stages {
        stage ('Compile Stage') {

            steps {
                  bat "mvn clean compile"
                  script{
                    hello.info('Maven clean install is done')
                }
                 }
        }

        stage ('Testing Stage') {

            steps {
                 bat "mvn test"
                 }
        }


        stage ('Package') {
            steps {
                 bat "mvn package"
               }
        }
    }
}
