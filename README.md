hello
aladdin mf
pipeline {
    agent any
    tools {
    maven 'MAVEN_HOME'
    }
    stages {

    stage('Git Clone') {
        steps {
            bat """
            rmdir /S /Q MavenJava 2>nul
            git clone https://github.com/ssvkotamraju/MavenJava.git
            """
        }
    }

    stage('Clean') {
        steps {
            bat "mvn clean -f MavenJava "
        }
    }

    stage('Install') {
        steps {
            bat "mvn install -f MavenJava "
        }
    }

    stage('Test') {
        steps {
            bat "mvn test -f MavenJava "
        }
    }

    stage('Package') {
        steps {
            bat "mvn package -f MavenJava "
        }
    }
}
}
