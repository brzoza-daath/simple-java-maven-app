pipeline {
    agent {
        docker {
            image 'maven'
            args '--mount source=~/.docker/mounts/maven,target=/root/.m3'
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
