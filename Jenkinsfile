pipeline {
	agent {
		node {
			label 'slave1'
			customWorkspace "/data/pipeline"
}
	}
	stages { 
			stage ('install-apache') {
			steps {
				sh "sudo yum install httpd -y"
 			}
		}
		stage ('deploy-index') {
			steps {
				sh "sudo cp -r index.html /var/www/html"
				sh "sudo chmod -R 777 /var/www/html"
 			}
		}
		stage ('restart-apache') {
			steps {
				sh "sudo service httpd restart"
 			}
		}
	}
}
 
	
