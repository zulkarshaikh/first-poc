pipeline
{
	agent any
	stages
	{
		stage('Complie')
		{
			steps
			{
				withMaven(maven : 'maven')
				{
					sh 'mvn clean compile'
				}
			}
		}


		stage('Test')
		{
			steps
			{
				withMaven(maven : 'maven')
				{
					sh 'mvn test'
				}
			}
		}


		stage('Deployment')
		{
			steps
			{
				withMaven(maven : 'maven')
				{
					sh 'mvn deploy'
				}
			}
		}
	}
}
