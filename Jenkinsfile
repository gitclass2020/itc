pipeline{
agent {node {label 'S1'}}

properties([parameters([choice(choices: ['checkout', 'invokeant'], description: 'Which stage you want to run', name: 'Stages')])])

stages{
	stage(checkout){
	steps{
	checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'eec141d1-ea8c-43f9-801a-cab104ec4365', url: 'https://github.com/gitclass2020/itc.git']]]	
	}

	}
 
	stage(invokeant){
	steps{
		
			 target('main')
		     buildFile('build.xml')
			 antInstallation('Ant 1.10')
		
    
 
 }
 }

 
 
 }

 }
 