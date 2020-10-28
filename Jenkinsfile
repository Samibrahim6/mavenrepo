pipeline{

    agent{label 'slave'}

stages{

stage('scm'){
steps{
checkout([$class: 'GitSCM', branches: [[name: '*/feat01']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'f1519b4d-8986-46c4-95be-eb4a02e3d8f4', url: 'https://github.com/Samibrahim6/mavenrepo.git']]])

     }    
         }

stage('package'){
steps{
sh 'mvn package'
     }
                }

stage('nexus'){
steps{
sh 'mvn deploy'
     }
              }

        }
        }
