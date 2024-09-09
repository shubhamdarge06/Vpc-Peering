# Vpc-Peering
VPC Peering Setup and Inter-VPC Connectivity !!!!!
Just done the vpc peering configuration

VPC PEERING is used for communicating with different vpc which is present in same region or different region.

The main component of vpc peering configuration is the route tables. The reason behind this is we will create the vpc peering connection but we also have to configure the routes so both the vpc's can accept the traffic / request from another vpc.

Also while configuring the route table we have to select the target which we created ( VPC PEERING CONNECTION ).

NOTE : All the steps are follow after creating both vpc's

>> Steps to create VPC PEERING : 
Go to VPC tab -> Peering Connection ( Left hand menu ) -> Create Peering connection -> Give name to the connection -> Select the Requester VPC (VPC ID) -> Select Account type (Same Account or Different) -> Select Region (Same Region or Different) -> Select the Accepter VPC (VPC ID) -> Click on Create Peering Connection.

>> After this accepter get the peering connection request :
Select the Vpc peering connection -> Actions -> Accept Request.

>> we have to configure the route tables for all subnets.

>> Route Table Configuration :
Go to VPC tab -> Route Table ( Left hand menu ) -> Select Route tables -> Select Route Table -> Edit Routes ->
Add route -> Enter Destination IP -> Select Target ( Peering Connection ) -> Select the Peering Connection -> Save Changes.

We also have to configure the Security Group.

YOU CAN NOW ACCESS THE INSTANCE LOCATED IN THE DIFFERENT VPC !

![Vpc_Peering](https://github.com/user-attachments/assets/4da45a4e-1e33-4eec-84ed-98a368f5850d)

