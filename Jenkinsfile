pipeline
{
	agent any
	stages
	{
		stage('Build Application')
		{
			bat 'mvn clean install -Dmunit.failIfNoTests=false'
		}
		stage('Deploy Application to Cloudhub')
		{
			bat 'mvn deploy -DmuleDeploy -Dmunit.failIfNoTests=false'
		}
		stage('Perform regression testing')
		{
			bat 'mvn deploy -DmuleDeploy -Dmunit.failIfNoTests=false'
		}					
	}
}