podTemplate(containers: [
	containerTemplate(name: 'jekyll', image: 'jekyll/jekyll:3.8'),
]) {
	node(POD_LABEL) {
	    stage('SCM Checkout') {
	      checkout scm
	    }
        stage('Run shell') {
            container('jekyll') {
                sh '/srv/jekyll build'
            }
        }
    }
}

// pipeline {
//     agent {
//         docker {
//             image 'jekyll/jekyll:3.8'
//             args '-u root:root -v "${WORKSPACE}:/srv/jekyll"'
//         }
//     }
//     stages {
//         stage('Test & Build') {
//             steps {
//                 sh '/srv/jekyll build'
//             }
//         }
//     }
// }
