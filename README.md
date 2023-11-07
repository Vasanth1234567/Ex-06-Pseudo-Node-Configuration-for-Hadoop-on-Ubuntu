# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/a6a47b23-faaa-40f1-b1fd-21406ba1fbe7)

2.	Install java1.8 in folder /usr/local<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/443c266d-b411-4731-b36a-d6d1de90f2e6)

3.	Install Hadoop<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/0fa3504e-fa0d-4dba-90c9-2c123410f217)

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/a9db00d1-d337-4442-ae2f-4135fff2dd7b)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/d509d6b7-917f-4e73-a95f-b391e5c92945)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes<br>


![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/593793e4-5507-4818-8578-8de56a0f9047)


7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml<br>

path ::	/usr/local/hadoop-2.5.1/etc/hadoop<br>

a)	hadoop-env.sh<br>
Include the following lines in hadoop-env.sh file<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/de77cac4-1574-4b77-bcd1-4241e022097d)


b)	core-site.xml<br>
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/ec762141-7a05-49d8-bee0-1d2e94fa032c)


 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags
<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/8f391342-5cdb-4f6e-8168-c1abed146181)

c)	mapred-site.xml<br>
 ![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/05510040-c2fc-4736-b12b-2e984a903746)


Include the following lines in mapred-site.xml file<br>
 ![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/39ea3c08-bcdd-418e-96d7-2ee9a8fab932)


d)	hdfs-site.xml<br>
Include the following lines in hdfs-site.xml file<br>

![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/6cdab3cb-39f3-4a4c-8999-e4519be0bc71)

e)	yarn-site.xml<br>
Include the following lines in yarn-site.xml file<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/929f611c-4676-469e-8ac1-dd2ec297b4cd)

8.	Format the Hadoop File system implemented on top of the local file system using<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/5fc47ed4-6f76-4d35-831d-ea30eed8bc67)

9.	Start Hadoop using<br>

![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/b9ee199f-eecc-40d1-be79-4a4251640f42)

Explore Hadoop using http://localhost:50070/ from the browser	<br>
 
10.	The commonly used HDFS Commands are as follows:<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/7a5f3095-6059-437f-a8fc-9c2534445255)


11.	Create a directory ‘/input’ in HDFS<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/47afa50e-1b00-4eee-b381-7a6ded99fe52)


12.	Copy the input files into the distributed file system<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/7275097c-ab9e-4608-8f7b-1c05528d51ce)

13.	Run some of the examples provided<br>

![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/de45c724-946f-424a-8c3d-31490076ed44)

14.	Examine the output files<br>
    ![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/1ce8ed28-9167-40d2-a099-d23d8a23009d)

Copy the output files from the distributed file system to the local file system and examine them:<br>
 ![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/ef028f34-02dd-4646-a953-c7b1207a0380)

or<br>
View the output files on the distributed file system<br>
![image](https://github.com/Vasanth1234567/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/86919099/903c9ccf-877a-4186-b202-f1f09bda39a7)

## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
