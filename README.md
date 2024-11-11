# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu
## AADHITHYA D-212222220001
## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/3de21905-1b6e-4007-a484-025e2b2f897b)

2.	Install java1.8 in folder /usr/local
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/110760be-ff06-4ae2-948a-6ade3b541d93)

3.	Install Hadoop
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/223bb242-300c-4cf0-acd2-41328b8914f9)

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/e13c3952-aa03-47f1-be13-e0e04e3f8c85)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/14fd3259-d177-4243-97f7-9dd17b6a45a2)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/48a3295f-4b5c-4c7a-a326-dd8285e68ef0)




$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh
Include the following lines in hadoop-env.sh file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/98ebad6d-5c08-436b-bbed-4238573cf4a1)


b)	core-site.xml
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/fb74aa85-efe1-4fe2-850e-796b98df41c6)


 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/eeb86eaa-4034-428f-a525-4736c43bccca)


c)	mapred-site.xml
 ![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/ac8d1033-784f-4bbd-abe1-e29a73046de6)


Include the following lines in mapred-site.xml file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/8b2042e7-935d-467d-85cd-4d28f68f92db)


d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/e05ddd7b-1e16-4009-a908-622c39cfdf14)


e)	yarn-site.xml
Include the following lines in yarn-site.xml file
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/e0aa4df4-324f-4901-8e41-1b9e0435265d)

8.	Format the Hadoop File system implemented on top of the local file system using
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/8d890e65-00d5-46c5-90c1-b3269d7dc3b1)

9.	Start Hadoop using
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/7f7e2257-08aa-43a3-a575-3fe32adfa833)


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/894711dc-85e8-41a8-a8dd-48d9039131d0)



11.	Create a directory ‘/input’ in HDFS
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/4bdf6eb3-ec0c-441a-8e70-a574d33b1396)


12.	Copy the input files into the distributed file system
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/ade0b0b7-946d-474f-b65a-dea4e3e85b3f)

13.	Run some of the examples provided
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/da758424-3904-4100-9445-39864cd519a9)


14.	Examine the output files
	![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/df1e440a-72ac-4534-af28-ef121b4c0768)

Copy the output files from the distributed file system to the local file system and examine them:
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/0e038242-5d89-47ee-9341-62c598f9fdf4)
 
or
View the output files on the distributed file system
![image](https://github.com/AjaysuryaS/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/114158396/7e834ba0-6915-4f28-ba99-fdf515d13b73)

## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
