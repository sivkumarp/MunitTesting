pipeline
{
 agent any 
 stages{
  stage('Build Application'){
   steps{
   bat 'mvn clean install -Denv=test'
   }
   }
 
 stage('Munit Testing'){
   steps{
   bat 'mvn test -Denv=test'
   }
   }
   
  stage('Deploy Application'){
   steps{
   bat 'mvn package deploy -DmuleDeploy -Denv=dev -nsu -DskipMunitTests'
   }
   }
 
  stage('Testing Application'){
   steps{
   bat 'C:\\Users\\smahadevanpillai\\AppData\\Roaming\\npm\\newman run C:\\Users\\smahadevanpillai\\Muleapi-Collection.postman_collection1.json --disable-unicode'
   }
   }
  }
}