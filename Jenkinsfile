pipeline {
    agent {
        label("nodejs")
    }

    stages {

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
