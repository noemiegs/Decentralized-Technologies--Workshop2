# Decentralized-Technologies--Workshop2

# Torrent

Q1 - Create a torrent containing this [image](https://cdn.futura-sciences.com/sources/images/Chaton.jpeg).

We create a first torrent and store it in a file :
```
torrent create Chaton.jpeg -o image.torrent
```

The torrent has been created : 

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/e29b72e2-3070-44cd-bd57-27df1e171598)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/3d8e4649-a4c0-4bad-811b-ea8bba13094a)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/1af81f33-9e7f-43c0-837b-beba45cd4bb0)


Q2 - Now copy the image to a new directory named partition1 and create a torrent of this folder. What do you observe?
```
torrent create partition1 -o partition1.torrent
```
The torrent has been created : 
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/fee8259d-03c6-4d0a-ac4d-bd484d84ac13)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/ee38d7b4-097c-40fb-83ee-78b1814beee8)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/1b4cd897-4be1-4e23-ae64-dcb0fb87382a)

We notice that the only things that have changed are the hash, and the path in the "files" too. Pieces stay the same. 

Q3 - Copy the partition1 folder and then generate the associated torrent. What do you observe?
```
torrent create partition2 -o outfile3.torrent
```
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/f0bccb41-652c-4e0a-9ce3-e2e63c18a876)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/ee439af5-8483-454d-905b-5b6cc96cab25)
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/0de41d55-c390-4db3-b04d-dbf44d702f36)

Like before, the only things that have changed are the hash, and the path in the "files" too. Pieces stay the same. 

# IPFS 

We install IPFS Desktop and IPFS CLI. 

Q1 - Upload the previous image to IPFS.

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/9768d6d4-357d-4692-8f51-6e53d3c4055b)
We get this CID : QmeJaufp9seXCpHMFwxX53P3oRQW8Ny1DduCXAxebEwxv7

When we inspect it : 
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/9922eca4-f859-4205-b94f-77730c004006)

Q2 - Now upload partition1 to IPFS. What do you observe compared to the torrent part?

We notice that the CiD has changed : QmPKRGW6BQ3i4Z4W4etVogYDRqoJRyFRCcD5FJrPKgNJPK. 
However, we notice that the image and the image inside the folder have the same hash. 
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/997ff745-58bf-440b-8b36-304c1346211c)

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/6d473973-5959-4da2-91ec-e637e3acd234)


Q3 - Copy the partition1 folder and then generate the associated torrent. What do you observe?

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/a2f088b0-2837-4330-a327-c3d42216e9ef)

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/061b8bb4-4cd5-4062-b086-20462371eca6)

We notice that like in the previous question, the CiD has changed and the image inside the folder still has the same hash. 


## Pinata

Thanks to the guide : https://docs.pinata.cloud/recipes/upload-a-file-to-pinata, I generated an API key and launched the index.js file with the ```node index.js``` command, and I had this output : 

![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/14ccc2c0-4020-4877-bed8-ce22b8386a2a)

And indeed, we can see that the file was well uploaded : 
![image](https://github.com/noemiegs/Decentralized-Technologies--Workshop2/assets/113913066/e01aa085-f18f-4df7-8c38-072e344e47a9)


