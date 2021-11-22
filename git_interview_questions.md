

# .......... Git Interview Questions For DevOps Engineer OR Software Engineer  .........

## By  Mamun Rashid :: https://www.linkedin.com/in/mamunrashid/ :: Please connect with me.

### Last Updated: 2021.11.21

##

#### 1.  Imagine you join our company. We have repo that has all our Terraform codes. I asked you to create some infrastructure using Terraform. Code for that would have to go through that repo.
####     What are the steps that you would go through?


#### Answer: 

       1. git clone
       2. git pull
       3. create a local branch from the Master branch or Development branch (depending on company policy)
       4. add code in that branch for this new infrastructure and create the infrastructure.
       5. commit and push the code into remote version of this new branch
       6. send in a Pull Request for merger (with master or develop)
       7. once the PR is approved, I will squash and merge 
       8. git fetch -all and git rebase

##

#### 2. What are some of your favorite tools on Unix? This comes up all the time.

#####   Your answer would be uniqe to your experience, but, here are some possibilities.

           a. grep
           b. find
           c. bash
           d. awk
           e. sed
           f. netstat
           g. nc
           h. ping
 
##

