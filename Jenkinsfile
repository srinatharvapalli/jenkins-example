pipeline {
    agent centos7-node

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_6_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven_3_6_0') {
                    sh 'mvn install'
                }
            }
        }
    }
}
