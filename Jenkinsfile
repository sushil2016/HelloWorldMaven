node
{
 stage("checkout"){
 git 'https://github.com/sushil2016/HelloWorldMaven.git'
 }
 stage("maven package"){
  def mavenHome=tool name: 'Maven', type: 'maven'
  sh "${mavenHome}/bin/mvn package"
 }
 stage("Build Docker image")
 {
  sh "docker build -t sushil2016/helloworld:1.0 ."
 }
 
  stage("Push Docker image")
 {
  sh "docker login -u sushil2016 -p kalia@2016"
  sh "docker push  sushil2016/helloworld:1.0 "
 }
 
 stage("Run Container on DevServer")
 {
  
  sh "docker run -p 8080:8080 -d name myapp sushil2016/helloworld:1.0"
  
 }
 
}
