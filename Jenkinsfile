pipeline {
    agent any
     tools {
        maven 'Maven3.6.3' 
    }

    stages {
        stage ('Compile Stage') {
           
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    echo "deploy"
                }
            }
        }
    }
}
