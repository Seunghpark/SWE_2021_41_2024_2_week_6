# SWE_2021_41_2024_2_week_6



**WEEK 4 Assignment**

Link
https://github.com/Seunghpark/SWE_2021_41_2024_2_week_4

Task
Complete isHappy function following the description below
Happy Number
Write an algorithm to determine if a number n is happy.

A happy number is a number defined by the following process:

Starting with any positive integer, replace the number by the sum of the squares of its digits.
Repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle which does not include 1.
Those numbers for which this process ends in 1 are happy.
Return true if n is a happy number, and false if not.

Constraints: 1 <= n <= 2^31- 1

My code:
"

    def isHappy(n):
    
      past = set()
      while n != 1 and n not in past:
        past.add(n)
        next = 0
    
        for digit in str(n):
          next += int(digit)**2
    
        n = next
      return n ==1
      
    #print(isHappy(1114))
"

"isHappy" function determines if a given integer n is a happy number, which repeatedly replaces the number with the sum of the squares of its digits until it equals 1 or falls into a cycle.








 --------



**Function Definition**



Input: Int n

Output: Bool. if n is a happy number == "True",  else False



"past" to track seen numbers for cycle detection.

Loop until "n" equals 1 or is found in "past"
  - Convert "n" to a str, then do the sum of the squares of its digits, and assign that sum back to "n".
       - If "n" is in "past", return False
          - Otherwise, add "n" to "past"



            
Return True if n becomes 1, indicating happiness.





__________________________________________________________________________________________________________________________


**WEEK 5 Assignment**


<img width="790" alt="Screenshot 2024-10-02 at 10 27 41 PM" src="https://github.com/user-attachments/assets/c4a369a4-6493-4c51-b02e-f7230df01979">

'

'

This command outputs the version details of the Ubuntu operating system running inside the Docker container named ossp-container

    docker exec ossp-container cat /etc/os-release
        


This command returns the version of Git installed in the Docker container


    docker exec ossp-container git --version


These commands show the version of Python installed, with -V being a shorthand for --version


    docker exec ossp-container python3 --version
    docker exec ossp-container python3 -V


This command fetches the binding configuration of the ossp-container Docker container


    docker inspect --format="{{ .HostConfig.Binds }}" ossp-container


