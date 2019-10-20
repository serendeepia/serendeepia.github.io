podTemplate(label: 'slave-ruby', containers: [
  containerTemplate(name: 'jnlp', image: 'docker.io/redhatcop/jenkins-slave-ruby', privileged: false, workingDir: '/tmp', args: '${computer.jnlpmac} ${computer.name}', ttyEnabled: false)
]) {
	node('slave-ruby') {
	    stage('SCM Checkout') {
	        checkout scm
	    }
	    stage('Build Code') {
		    sh """
		        gem update --system
		        gem install bundler
		        bundle install
		        bundle exec jekyll build
	        """
		}
	}
}
