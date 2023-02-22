# Phonepe-Data-visualization-(2018-2022)
Hi friends this is the app i created to analyse Phonepe pulse data which i get through Phonepe pulse github repo.Then I deployed this app in streamlit.Enjoy the code 😉
![alt_text](https://media.licdn.com/dms/image/C5612AQGdCw8CZhcuEQ/article-cover_image-shrink_600_2000/0/1607024381761?e=2147483647&v=beta&t=tKCyrHlbMu3A5SX-dJAR799b6Kxu1x81QbTM904m1QQ)
**Please install requirements.txt.**
>[My app link](https://thiruvenkatam007-phonepe-data-visualization-2018---main2-iax51p.streamlit.app/)

### First lets extracts datas from the github and convert it into csv files
*This is the dataset i used in my streamlit web application to visualize datas*
>[Phonepe pulse github repo](https://github.com/PhonePe/pulse#readme)

After cloning files from github repo i created a _for_ loop to loop through each folder and get datas from it and then append it to a dataframe to make it easy to covert to csv.

![data_extraction](https://user-images.githubusercontent.com/113424127/220614411-96c8d674-306f-4f37-83b3-f35f02443be2.png)

In this above code we can see that in each step we go through the folders and we also setting the folder name as a value for dictionary.

Now we want to repeat this process for all respective folders then we can get all the data in our desired format of csv.

### After extracting the data we need to upload it into Mysql
To insert datas into Mysql i used sqlalchemy(in order to establish connection you want pymysql also) 

#### In order to insert csv to Mysql we need to establish connection to Mysql server

![sql_connection](https://user-images.githubusercontent.com/113424127/220616841-aa01942b-952d-4f67-a845-1a3e95a0c8a7.png)

#### After connection we need to create table then we can insert csv files to Mysql database

![sql_insert](https://user-images.githubusercontent.com/113424127/220617416-677c2928-472e-4d8b-9f1a-2ad453f6424f.png)

To see full code see in mysqlinsert.ipynb file 
Repeat the above process for all csv files to insert into your Mysql database

Then after inserting all my files to Mysql database.
I created a new file named main.py to create a app using streamlit.

# My app preview
![appimage](https://user-images.githubusercontent.com/113424127/220618749-2827a7a7-566c-40f5-b78d-8f155f068c57.png)

# Geo-visualization of Transaction datas

To see detailed code to use plotly for Geo visualization see main.py (Geo-visualization of transacion data section)
![geo visualization](https://user-images.githubusercontent.com/113424127/220619224-e6a6de0f-c2d1-4bfa-b4f1-31c8499dc1ba.png)

# User device analysis od Phonepe data
## TREEMAP ANALYSIS
![userdevice](https://user-images.githubusercontent.com/113424127/220620570-64fefa3d-9d88-4650-a7ff-6eca47d6bf54.png)
## BAR CHART ANALYSIS
![user](https://user-images.githubusercontent.com/113424127/220620707-99800e30-9b26-445a-86d7-3604a69c6d68.png)

# Payment type analysis
## PIE CHART ANALYSIS
![paymentpie](https://user-images.githubusercontent.com/113424127/220621370-ebb279f5-8c7c-4c5d-9c9d-41db47d4556d.png)
## BAR CHART ANALYSIS
![paymentbar](https://user-images.githubusercontent.com/113424127/220621500-6dad69df-24f2-494c-ad97-6378adab91b9.png)

### In side bar you can see overall India's data visualization for all datas.


