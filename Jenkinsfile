pipeline{
        agent {
		       label {
	                 label"build in"
                     cutomerWokrspace "/mnt/project"					 
			     }
		       }
		stages{
	          stage("install httpd"){
                  steps{
				      sh "yum install httpd -y"  
				  }			  
			   }
			   stage("start httpd"){
                  steps{
				      sh "service httpd start"  
				  }			  
			   }
			   stage("deploy html"){
                  steps{
				      sh "cp -r index.html/var/www/html"
					  sh "cp -r dev.html/var/www/html"
					  sh "chmod -R 777 /var/www/html"
					  
					  
				  }			  
			   }	
		
		}	   


}
