pipeline {
   agent any
   
   tools {
       'Maven 3.9.6'
   }
   
   stages{
       stage('build'){
           steps{
               echo 'compile maven app'
               sh 'maven compile'
           }
       }
       stage('test'){
           steps{
               echo 'test maven app'
               sh 'maven clean test'
           }
       }
       stage('package'){
           steps{
               echo 'package maven app'
               sh 'mvn package -DskipTests'
           }
       }
   }
  
  post{
     always{
         echo 'This pipeline is completed..'
     }
  } 
}
