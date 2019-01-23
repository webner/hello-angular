pipeline {
    agent {
        label("angular")
    }

    stages {

        stage("npm install") {
            steps {
                sh "npm install"
            }
        }

        stage("build") {
            steps {
                sh "ng build"
            }
        }

        stage("test") {
            steps {
                sh "ng test"
            }
        }

        stage("build image") {
            steps {
                sh "oc start-build hello-angular -F --from-dir=dist/hello-angular"
            }
        }

    }

}
