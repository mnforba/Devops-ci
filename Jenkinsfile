node
{
 
  stage("CheckOutCodeGit")
  {
   git branch: 'master', credentialsId: '65fb834f-a83b-4fe7-8e11-686245c47a65', url: 'https://github.com/bhaskar0504/node-js-application.git'
 }
 
 stage("Build")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install'
	}
 }
 stage("build")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm run build'
	}
 }
 /*
 stage("LintTest")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install eslint --save-dev'
        sh 'npm run lint'
	}
 }
 */
 stage("PrettierTest")
 {
 nodejs(nodeJSInstallationName: 'nodejs15.2.1') {
        sh 'npm install prettier --save-dev'
        sh 'npm run prettier'
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
