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
                sh "echo test"
            }
        }

        stage("deploy") {
            steps {
                sh "oc status"
            }
        }

    }

}
