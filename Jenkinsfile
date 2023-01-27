pipeline{
    agent any
    tools {
          maven 'Maven' 
        }
         

        stages
        {
            stage ('cloning git')
            {
                steps
                {
                    git branch: 'main', url: 'https://github.com/harshasampgit/helloworld.git'
                }

            }
            
            stage('validate') 
            {
                steps 
                {
		            sh 'mvn validate'
		
                }
            }
            
            stage ('build')
            {
                steps
                {
                    sh "mvn install"
                }

            }

        }
    }
