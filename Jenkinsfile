pipeline {
    agent any

    stages {
        stage('git-checkout') {
            steps {
            
           checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/nirajchaul/spring-petclinic.git']]])  
                    }
        }
        
        
        
        stage('init') {
            steps {
                 
               echo 'Hello World!'
                
            }
        }
        
        
        stage('plan') {
            
            steps {
             
                 echo 'Hello Plan!'          
        }
                
            }
        }
        
        
        

    }



