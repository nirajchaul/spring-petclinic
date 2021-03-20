pipeline {
    agent any
    tools { 
        maven 'Maven 3.0.5' 
        jdk 'jdk8' 
    }

    stages {
        stage('git-checkout') {
            steps {
            
           checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/nirajchaul/spring-petclinic.git']]])  
                    }
        }
        
        
        
        stage('init') {
            steps {
                 
              mvn test
                
                
            }
        }
        
        
        stage('plan') {
            
            steps {
             
                 mvn compile         
        }
                
            }
        
        
        stage('build') {
            
            steps {
             
                 mvn build         
        }
                
            }
        
        
        }
        
        
        

    }



