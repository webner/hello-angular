pipeline {
    agent {
        label("nodejs")
    }

    stages {

        stage("install angular cli") {
            steps {
                sh "npm install -g @angular/cli"
            }
        }

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
