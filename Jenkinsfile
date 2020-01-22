pipeline
{
 agent any 
 stages{
  stage('Build Application'){
   steps{
   bat 'mvn clean install -Dmule.env=test'
   }
   }
 
 stage('Munit Testing'){
   steps{
   bat 'mvn test -Dmule.env=test'
   }
   }
   
  stage('Deploy Application'){
   steps{
   bat 'mvn package deploy -DmuleDeploy -Dmule.env=dev'
   }
   }
 
  stage('Testing Application'){
   steps{
   bat 'C:\\Users\\smahadevanpillai\\AppData\\Roaming\\npm\\newman run C:\\Users\\smahadevanpillai\\Muleapi-Collection.postman_collection1.json --disable-unicode'
   }
   }
  }
}