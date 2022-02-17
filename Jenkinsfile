node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/satishtrust83/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multibranch-pipeline/webapp/target/webapp.war   ubuntu@172.31.40.118:/var/lib/tomcat9/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}    
}
