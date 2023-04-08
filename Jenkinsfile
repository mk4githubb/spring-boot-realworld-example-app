pipeline {
    agent any

    stages {
        // First Stage
        stage("Clean up"){
            steps{
                deleteDir()
            }
        }

        // Second stage
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/mk4githubb/spring-boot-realworld-example-app"
            }
        }

        // Third stage
        stage("Build"){
            steps {
                dir("spring-boot-realworld-example-app"){
                    sh "gradle clean build"
                }
            }
        }

        // Fourth stage
        stage("Test"){
            steps {
                dir("spring-boot-realworld-example-app"){
                    sh "gradle test"
                }
            }
        }
    }
}
