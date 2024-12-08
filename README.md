# Shell_Scripting_For_DevOPS

>> Shell – It is utility which allow us to talk to kernel . 

>> Bash – It is kind of shell. It is more popular shell. Born again shell. It is end with .sh  .

>> sh – It is also shell. 

>> write the first bash scripting .

shebang - #!/bin/bash  - This will always come whenever we start script .

>>vi hello.sh and write below script 

#!/bin/bash

echo "Gabbar: Kitne aadmi the"

echo "Sambha: 2 sarkar"



>> then chmod 777 hello.sh

Below is the output of script:
>> ./hello.sh
root@ip-172-31-45-40:~/Scripts# ./hello.sh
Gabbar: Kitne aadmi the
Sambha: 2 sarkar


==================================================================================


>>Second script 

 #!/bin/bash

echo "Gabbar: Kitne aadmi the"

echo "Sambha: 2 sarkar"

echo "Gabbar: Kitna bja hai"

date

echo "Gabbar : kitne baje se class chal rha hai"

uptime


>> output :

root@ip-172-31-45-40:~/Scripts# ./hello.sh
Gabbar: Kitne aadmi the
Sambha: 2 sarkar
Gabbar: Kitna bja hai
Tue Oct 15 10:20:43 UTC 2024
Gabbar : kitne baje se class chal rha hai
 10:20:43 up 4 min,  2 users,  load average: 0.02, 0.13, 0.07

==============================================================================
                                                   Another script where we can write Comment .

#!/bin/bash   

#this is sholay story by Rajan


<<Comment

This is multiline comment 

Comment

echo "Gabbar: Kitne aadmi the"
echo ""
echo "Sambha: 2 Sarkar"
echo ""
echo "Gabbar: Kitna bja hai"
echo ""
date
echo ""
echo "Gabbar: kitne der se class chal rha hai"
echo ""
uptime


output of script :

root@shellMachine:/home/ubuntu/script# ./hello.sh 
Gabbar: Kitne aadmi the

Sambha: 2 Sarkar

Gabbar: Kitna bja hai

Mon Dec  2 02:34:07 UTC 2024

Gabbar: kitne der se class chal rha hai

 02:34:07 up 38 min,  1 user,  load average: 0.00, 0.00, 0.00 

====================================================================
                                                    Variables and Constant  

>> Variable – Anything that is vary called variable .

a = 2   - Here a is variable and 2 is constant .

write the below script :


>> variable.sh 

#!/bin/bash


<<Note

This is demo for variables.

Note

Name="Rajan"

echo "My name is $Name"

Output :

root@shellMachine:/home/ubuntu/script# ./variables.sh 
My name is Rajan

==============================================================================
                                                                  >> Another script for variables


#!/bin/bash


<<Note

This is demo for variables.

Note

Name="Rajan"

echo "My name is $Name"

echo "What is your name"

Name2="Anoop"

echo "My name is $Name2


output :

root@shellMachine:/home/ubuntu/script# ./variables.sh 
My name is Rajan
What is your name
My name is Anoop



>> We can ask input from users as well :



#!/bin/bash


<<Note

This is demo for variables.

Note

echo "Enter the name"

read Name

echo "My name is $Name"

echo "What is your name"

read Name2

echo "My name is $Name2"

Output :

 

>> vi greeting.sh

#!/bin/bash

# Define variables
USER_NAME="User"
GREETING="Hello"
COUNTER=1

# Greeting the user
echo "$GREETING, $USER_NAME!"

# Loop to count from 1 to 5
echo "Counting from 1 to 5:"
while [ $COUNTER -le 5 ]
do
  echo "$COUNTER"
  COUNTER=$((COUNTER + 1))
done

# Conditional statement
if [ $COUNTER -gt 5 ]; then
  echo "Count complete!"
else
  echo "Count failed."

fi



>> Explanation for above script:

#!/bin/bash  - This line indicates that the script should be run using the Bash shell.


USER_NAME="User"
GREETING="Hello"
COUNTER=1 

These lines define three variables:
•	USER_NAME is set to "User".
•	GREETING is set to "Hello".
•	COUNTER is initialized to 1.
# Greeting the user
•	echo "$GREETING, $USER_NAME!"

This line outputs a greeting message to the user by combining the GREETING and USER_NAME variables. It will display: Hello, User!
# Loop to count from 1 to 5
echo "Counting from 1 to 5:"
while [ $COUNTER -le 5 ]
do
  echo "$COUNTER"
  COUNTER=$((COUNTER + 1))
done

•	This section starts a loop:
•	It first prints "Counting from 1 to 5:".
•	The while loop checks if COUNTER is less than or equal to 5 (-le stands for "less than or equal").
•	Inside the loop:
•	It prints the current value of COUNTER.
•	It increments COUNTER by 1 using the expression COUNTER=$((COUNTER + 1)).


•	The loop continues until COUNTER exceeds 5, resulting in the numbers 1 to 5 being printed.
# Conditional statement
if [ $COUNTER -gt 5 ]; then
  echo "Count complete!"
else
  echo "Count failed."
fi


•	This part contains a conditional statement:
•	The if checks if COUNTER is greater than 5 (-gt stands for "greater than").
•	Since the loop increments COUNTER to 6 after counting to 5, the condition will be true.
•	If true, it prints "Count complete!".
•	If never true (which in this script will not happen), it would print "Count failed."





==================================================================================
                                                       Here we can use -p (prompt)




#!/bin/bash


<<Note

This is demo for variables.

Note

read -p "Enter the name" Name


echo "My name is $Name"

echo "What is your name"

read Name2

echo "My name is $Name2"
~                             


Outputs :

root@shellMachine:/home/ubuntu/script# ./variables.sh 
Enter the name Rajan
My name is Rajan
What is your name
Noora
My name is Noora

=====================================================================================
                                               //   Below script will install NGINX and enable it also //


#!/bin/bash


<<Note

This script will install NGINX

Note

echo "********************Installing_NGINX********************************"


sudo apt-get update

sudo apt-get install nginx -y

sudo systemctl start nginx

sudo systemctl enable nginx

sudo nginx -v


echo "**********************NGINX_Installed**********************************"

=====================================================================================
Arguments : We can pass any arguments 


>> #!/bin/bash


<<Note

This script will install any package.

./Install_package.sh <arg>

Note

echo $1

echo "********************Installing $1********************************"


sudo apt-get update

sudo apt-get install $1 -y

sudo systemctl start $1

sudo systemctl enable $1


echo "**********************Installed $1**********************************" 

>> Outputs Below :  In Below script we can pass any arguments and it will work accordingly .


 



=====================================================================================



#!/bin/bash

<<disclaimer

Is kahani ke sabhi patr and Ghatnaye kalpnic

disclaimer


read -p "Enter Gabbar's Dilogue:" gb

read -p "Enter Thakur's Dilogue:" th

echo "$gb"

echo "$th"


Output :

root@ip-172-31-45-40:~/Scripts# ./Gabbar_Thakur.sh
Enter Gabbar's Dilogue:ye hath hmko de thakur
Enter Thakur's Dilogue:Nahi
ye hath hmko de thakur
Nahi


=====================================================================================
                                           Conditional Statement  If and Else 

>> If and Else are conditional statements ;

>> scripts below :

#!/bin/bash


<<disclaimer

Iss kahani ke sabhi patr and ghatnaye kalpnic hai 

disclaimer

read -p "Enter gabbar's dialogoue" gb

read -p "Enter Thakur's dialogue" th

echo "$gb"
echo "$th"

if [[ $th == "nahi" ]];

then

echo "Jai veeru ki entry and bhsad"

else
echo "chop chop"

fi

echo "sholay kahtam"

 


====================================================================================

                                                                // Process for take the BKP //


./Install-pkg.sh zip  - For install the zip

zip -r backup.zip /home/ubuntu/script    - This will compress the script and store in backup.zip

 


>>  Below script will show date in format.

#!/bin/bash


<<Note

This will take backup of any destination path given in arguments 

./backup.sh /home/ubuntu/script

Note

echo "$(date '+%Y-%m-%d')"



Output :

root@shellMachine:/home/ubuntu/script# ./backup.sh 
2024-12-02


>>>Below script will take the backup with timestamp 

vi backup.sh


#!/bin/bash


<<Note

This will take backup of any destination path given in arguments 

./backup.sh /home/ubuntu/script

Note

timestamp="$(date '+%Y-%m-%d-%H-%M-%S')"

backup_dir="${timestamp}_backup.zip"

zip -r $backup_dir $1

echo "Backup complete"

output :

 

===================================================================

                                            //CRONE //

>>  Use this website for use the crone in better way - https://crontab.guru/#5_4_*_*_1

>> 

                                      


#!/bin/bash


<<Note

This will take backup of any destination path given in arguments 

./backup.sh /home/ubuntu/script

Note
function show_date {
echo "Today is : $(date '+%Y-%m-%d-%H-%M-%S')"
}
function create_backup {

timestamp="$(date '+%Y-%m-%d-%H-%M-%S')"

backup_dir="/home/ubuntu/backups${timestamp}_backup.zip"

zip -r $backup_dir $1

echo "Backup complete"

}
show_date
show_date
show_date
show_date
create_backup


Outputs:

 


===================================================================



                                                                                                                             


                
