pipeline {
    agent any
    tools {
        maven 'Maven 3.5.3'
        jdk 'jdk1.8.0_161'
    }
    stages {
        stage ('initialize') {
            steps {
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
