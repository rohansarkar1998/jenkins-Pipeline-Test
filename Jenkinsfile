
pipeline {
    agent any

    environment {

            serverDetails = credentials('tomcat_deployer')

    }

    stages {
        stage("build") {

        steps {
            echo 'build application'
            echo "the credential is ${serverDetails}"
            sh "chmod +x pipelineTest.sh"
            sh "./pipelineTest.sh ${serverDetails}"
        }
    }

         stage("test") {

        steps {
            echo 'test application'
        }
    }
    
         stage("deploye") {

        steps {
            echo 'deploye application'
        }
    
    } 
}


}
