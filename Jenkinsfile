/* properties([parameters([string(defaultValue: '', description: '', name: 'RMNumber', trim: false)])]) */

pipeline {
     agent any
    
stages {
   stage('Build'){
fileOperations([fileCopyOperation(excludes: '', flattenFiles: false, includes: '*.json', targetLocation: 'D:\\Test1')])
   }
stage('Deploy'){
            def lst = []
            def count = new File("D:/Test1/").listFiles().size()
            if (count>0){
            println("there arenumber of files to be deployed" +count)
                for (i=1;i<=count;i++)
                        {
                            println("executing the"+i+"job")
                                            build 'freestyle'
               
                        } 
                        }
             else
             {println("there arenumber of files to be deployed" +count)}

}
    /*stage('Version'){
       echo "the RM number to be versioned is: ${params.RMNumber}"
        
    }*/
}
}
