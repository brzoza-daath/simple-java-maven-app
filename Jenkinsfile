pipeline {
    agent {
        docker {
            image 'maven'
            args '-v maven:/root/.m3'
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
