pipeline{
 agent any

 stages{
   
   stage('build'){
    
    steps{
	echo 'building'

	sh 'ls'
    }
   
   }

   stage('test')
   {
     steps{
	echo "testing"
	sh 'cat file2.txt'

     }
   }

   stage('Result'){
     steps{

	echo "Result is successful"
     }
   
   }


 }

}
