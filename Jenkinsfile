node
{
 
  stage("CheckOutCodeGit")
  {
   git branch: 'main', credentialsId: 'GIT_HUB_CREDENTIALS', url: 'https://github.com/mnforba/Devops-ci.git'
 }
 
 stage("Build")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install'
	}
 }
 
 stage("LintTest")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install eslint --save-dev'
        sh 'npm run lint'
	}
 }
 
 stage("PrettierTest")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install prettier --save-dev'
        sh 'npm run prettier'
	}
 }
 stage("Test")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'CI=true npm run test'
	}
 }
 stage("build")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm run build'
	}
 }
 /*
  stage('ExecuteSonarQubeReport') {
     nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm run sonar'
    }
      
        } 
		
    stage('UploadintoNexus') {
       nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
          sh 'npm publish'
      }
      
          }	
 
 stage('RunNodeJsApp')
 {
 //sh "./scripts/run.sh"
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm start &'
    }
}    
 */   
}
