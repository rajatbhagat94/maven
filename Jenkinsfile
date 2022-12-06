node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /var/lib/jenkins/workspace/webhook/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat9/webapps/abcenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'scp /var/lib/jenkins/workspace/webhook/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat9/webapps/abcenv.war'
	}
}
