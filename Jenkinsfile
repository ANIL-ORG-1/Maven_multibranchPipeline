node('master') 
{
    stage('ContinuousDownload_Loans')
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    } 
    stage('ContinuousBuild_Loans')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment_Loans')
    {
        sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.83.143:/var/lib/tomcat8/webapps/qaenv.war'
    }
    
    
    
    
}
