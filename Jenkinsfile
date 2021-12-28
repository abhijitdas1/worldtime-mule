pipeline
{
	agent any
	stages
	{
		stage('Build Application')
		{
			steps
			{
				bat 'mvn clean install -Dmunit.failIfNoTests=false'
			}
		}
		
		
		stage('Deploy Application to Cloudhub')
		{
			steps
			{
				bat 'mvn deploy -DmuleDeploy -Dmunit.failIfNoTests=false'
			}				
		}
		stage('Perform regression testing')
		{
			steps
			{
				bat 'C:\\Users\\abhijitadas\\AppData\\Roaming\\npm\\newman run C:\\Users\\abhijitadas\\world-timezone.postman_collection.json -r htmlextra --reporter-htmlextra-export C:\\Users\\abhijitadas\\ --disable-unicode'
			}				
		}					
	}
}