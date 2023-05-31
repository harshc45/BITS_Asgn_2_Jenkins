pipeline {
    agent any
    tools {
        maven 'Maven 3.6.1'
        jdk 'jdk 17'
    }
    stages {
    stage('Initialize') {
        steps {
            sh '''
            echo "PATH = ${PATH}"
            echo "JAVA_HOME" = ${JAVA_HOME}
            echo "MAVEN_HOME = ${MAVEN_HOME}"
        '''
        }
    }

    stage('Build') {
        steps {
                echo 'BUILD'
                sh 'mvn clean install -DskipTests=true'
            }
        }
        stage('Test') {
            steps {
                echo 'TEST'
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'PACKAGE'
                sh 'mvn package'
            }
        }
        stage('Deploy') {
        steps {
            echo 'DEPLOY'
        }
    }
    }
}
