pipeline {
    agent windows-node

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven-3.6.0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven-3.6.0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven-3.6.0') {
                    sh 'mvn install'
                }
            }
        }
    }
}
