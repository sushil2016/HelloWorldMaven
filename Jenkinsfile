node
{
 stage("checkout"){
 git 'https://github.com/sushil2016/HelloWorldMaven.git'
 }
 stage("maven package"){
  def mavenHome=tool name: 'Maven', type: 'maven'
  sh "${mavenHome}/bin/mvn package"
 }
 
}
