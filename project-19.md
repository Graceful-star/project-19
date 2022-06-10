# Documentation of project19

## Step1
1. I installed packer 
   ![Project19](images/pro1.PNG)

2. I changed directory into my packer folder in my workspace
    
    ![Project19](images/pro2.PNG)

3. I ran `packer fmt` to format the files in my folder
     
     ![Project19](images/pro3.PNG)
    
4. Then I ran the build command for my bastion server

     `packer build bastion.pkr.hcl`

     ![Project19](images/pro4.PNG)
     ![Project19](images/pro5.PNG)

5. I ran the build command for nginx server as well
    
    `packer build nginx.pkr.hcl`

    ![Project19](images/pro6.PNG)
    ![Project19](images/pro7.PNG)

6. I also ran the build command for ubuntu server
    
    `packer build ubuntu.pkr.hcl`

    ![Project19](images/pro8.PNG)
    ![Project19](images/pro9.PNG)

7. I ran the build command for web server also

    `packer build web.pkr.hcl`

    ![Project19](images/pro10.PNG)
    ![Project19](images/pro11.PNG)
   

8. I confirmed the AMIs that were created on my aws console

   ![Project19](images/pro15.PNG)

9. I inserted the AMIs that were created in my 'terraform.auto.tfvars' file

     ![Project19](images/pro12.PNG)

10. I created a new terraform account and configured it

     ![Project19](images/pro13.PNG)
     ![Project19](images/pro14.PNG)

11. I made the necessary changes to my terraform folder then I pushed the changes to my gitlab repository
     
     ![Project19](images/pro16.PNG)
     ![Project19](images/pro17.PNG)

12. I started a plan and I applied it on my terraform console

     ![Project19](images/pro18.PNG)
     ![Project19](images/pro19.PNG)
     ![Project19](images/pro20.PNG)
     ![Project19](images/pro21.PNG)
     ![Project19](images/pro22.PNG)
     ![Project19](images/pro23.PNG)
     ![Project19](images/pro24.PNG)
     ![Project19](images/pro25.PNG)

13. I confirmed what terraform created on my aws console
     
     ![Project19](images/pro26.PNG)
     ![Project19](images/pro27.PNG)
     ![Project19](images/pro28.PNG)
     ![Project19](images/pro29.PNG)
     ![Project19](images/pro30.PNG)
     ![Project19](images/pro31.PNG)
     ![Project19](images/pro32.PNG)
     ![Project19](images/pro33.PNG)
     ![Project19](images/pro34.PNG)
     ![Project19](images/pro35.PNG)
     ![Project19](images/pro36.PNG)
     ![Project19](images/pro37.PNG)
     ![Project19](images/pro38.PNG)
     ![Project19](images/pro39.PNG)
     ![Project19](images/pro40.PNG)
     ![Project19](images/pro41.PNG)

14. I commented out the command for creating listeners, attaching external loadbalancer to autoscaling group 
    
    ![Project19](images/pro42.PNG)
    ![Project19](images/pro43.PNG)

15. I went to my terraform console to plan and apply the changes
     
     ![Project19](images/pro44.PNG)


## Step2

1. I logged into my bastion server

2. I configured aws

3. I exported the ansible-config path

4. I tried running the inventory command in my inventory directory at first but it wasn't successful
    
    ![Project19](images/pro45.PNG)

5. I troubleshooted and realized I didn't install boto3 and botocore properly si I did the needful
    
    ![Project19](images/pro46.PNG)

6. So I ran the ansible command again and it was successful
     
     ![Project19](images/pro47.PNG)

7. Then I ran the ansible-playbook command too and it was successful
     
     ![Project19](images/pro48.PNG)
     ![Project19](images/pro49.PNG)


# Step 3

1. I ssh into my nginx server through my bastion server

   ![Project19](images/pro50.PNG)

2. I ssh into my wordpress server through my bastion server

   ![Project19](images/pro51.PNG)

3. I checked if the server was running on my localhost
  
  ![Project19](images/pro52.PNG)
  ![Project19](images/pro53.PNG)

4. It didn't connect properly so I made some changes in "wp-config.php"
    
    ![Project19](images/pro54.PNG)

5. I ran the `curl -v localhost` command again and it worked

    ![Project19](images/pro55.PNG)

6. I ssh into tooling server through bastion server
    
    ![Project19](images/pro56.PNG)

7. I checked if the server was running perfectly on my localhost

    ![Project19](images/pro57.PNG)
    ![Project19](images/pro58.PNG)

8. I went to my Route53 and copied my wordpress link 
     
     ![Project19](images/pro59.PNG)

9. I opened the link on my incognito tab
     
     ![Project19](images/pro60.PNG)
     ![Project19](images/pro63.PNG)

10. I went to my Route53 zone and copied my tooling link

    ![Project19](images/pro61.PNG)
    
11. I opened the link on my browser

    ![Project19](images/pro62.PNG)

12. I opened my jenkins link on my browser too and it worked

    ![Project19](images/pro64.PNG)

13. I destroyed the infrastructure when I  finished what I was doing

    ![Project19](images/pro65.PNG)
