pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
    stages {
        stage ('Compile Stage') {

            steps {
                  bat "mvn clean compile"
               //   script{
                 //   hello.info('Maven clean install is done')
               // }
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
