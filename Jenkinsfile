podTemplate(label: 'slave-ruby', cloud: 'openshift', serviceAccount: "jenkins", containers: [
  containerTemplate(name: 'jnlp', image: 'docker.io/redhatcop/jenkins-slave-ruby', privileged: false, workingDir: '/tmp', args: '${computer.jnlpmac} ${computer.name}', ttyEnabled: false)
]) {
	node('slave-ruby') {
		node('jekyll') {
	        stage('SCM Checkout') {
	            checkout scm
	        }
	        stage('Build Code') {
		        sh """
		            bundle install
		            gem env
		            bundle exec jekyll build
	            """
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
