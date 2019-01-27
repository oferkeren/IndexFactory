pipeline {
    agent { label 'slave' } 

    stages {
        stage('checkout') {
            steps {
                //deleteDir()
                checkout scm
            }
        }
    stage('npm mongoDB') {
            steps {
                bash '''npm install mongodb --save'''
            }
        }    
    stage('sed Line') {
            steps {
                bash '''sed -i \"461s/.*/self.s.topology.cursor(self.s.db.databaseName+".system.profile", { find: 'system.profile', query: {}}, {}).toArray(callback);/"  $WORKSPACE/node_modules/mongodb/lib/admin.js'''
            }
        }     
    }
}
 
