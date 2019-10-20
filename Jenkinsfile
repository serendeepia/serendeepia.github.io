pipeline {
    agent {
        docker {
            image 'jekyll/jekyll:3.8'
            args '-u root:root -v "${WORKSPACE}:/srv/jekyll"'
        }
    }
    stages {
        stage('Test & Build') {
            steps {
                sh '/srv/jekyll build'
            }
        }
    }
}
