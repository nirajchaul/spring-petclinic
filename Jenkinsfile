pipeline {
    agent any
   /* tools { 
        maven 'Maven 3.0.5' 
        jdk 'jdk8' 
    }*/

    stages {
        stage('git-checkout') {
            steps {
            
           checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/nirajchaul/spring-petclinic.git']]])  
                    }
        }
        
        
        
        stage('init') {
            steps {
                 
              sh 'mvn -eX test'
                
                
            }
        }
        
        
        stage('plan') {
            
            steps {
             
                sh 'mvn compile'         
        }
                
            }
        
        
        stage('build') {
            
            steps {
             
                 sh 'mvn build'        
        }
                
            }
        
        
        }
        
        
        

    }



