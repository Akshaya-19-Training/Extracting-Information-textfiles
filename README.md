                                                            # Extracting-Information-textfiles
    
    1.Extract log.tar.gz
    2.Look for unauthorized connection attempts
    3.Extract the usernames an attacker tried to use
    4.Create a file containing these names (and make it organized)
   
    
                                                             #solutions
                                                             
    1.tar -xvf log.tar.gz  // this create auth.log file
    2.less auth.log  // to check unauthorized connection attempts
      cat auth.log | grep "input userauth request"   //will give output which contains userauth request
   3. cat auth.log | grep "input userauth request"|awk '{print $9}'
   4. cat auth.log | grep "input userauth request"|awk '{print $9}'|sort -u > users.txt
   
