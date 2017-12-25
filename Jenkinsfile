
pipeline {
            agent any
            tools 
            {
                maven 'maven_3_5_0'
            }
            stages 
            {
                stage ('Initialize') 
                {
                    steps 
                    {
                        git " https://github.com/nurperiutlu/Patientmanagement.git"
                               
                    }
                }
                 
                stage ('Build') 
                {
                    steps 
                    {
                        bat 'mvn verify' 
                    }
                    
                }
                stage ('Test')
                {
                            steps
                            {
                                        bat 'mvn test'
                            }
                }
               stage ('Deployment')
                {
                            steps
                            {
                                        bat 'mvn deploy'
                            }
                }
            }
}
