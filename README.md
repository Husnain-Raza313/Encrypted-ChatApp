# Encrypted-ChatApp
A mini chatapp that takes client's PC name and mac address and encrypts the chat by using a certain formula.
Encrypted CHATAPP
![image](https://user-images.githubusercontent.com/85040899/120102725-dedfd200-c165-11eb-9b7c-734a6028f7df.png)


Developed by: Husnain Raza

Tools Required
•	Wireshark: Packet Analysis Tool
•	Netbeans and JDK(Java Development Kit)

•	Language Used:
	
Java 


How it Works!!




<b>Note: Server side must be run first followed by the Client Side and the first two messages from the Server must be “what is your computer name?” and “what is your mac address?” respectively, to initiate the encryption. (I tried to explain everything properly, but in case there is any confusion or any query or any need of explanation, please contact me on gmail hussnainrezamir72@gmail.com”) </b>

At the initiation of the program and establishment of connection, server is supposed to ask the client “what is your computer name?”, to which client will automatically reply with its computer name.


 ![image](https://user-images.githubusercontent.com/85040899/120102767-12baf780-c166-11eb-94a9-6cbae5453bdc.png)


Then Server will request for client’s mac address by stating “what is your mac address?” , to which client will reply with its mac address automatically
 

![image](https://user-images.githubusercontent.com/85040899/120102777-18b0d880-c166-11eb-9356-2f27776364b8.png)


The key will be generated at both sides’ backends( visible on console):
![image](https://user-images.githubusercontent.com/85040899/120102790-29f9e500-c166-11eb-8d15-a02ec67ef007.png)

 
Since the initiation, up until the sending of Mac Address, the chat would not be encrypted and it can be checked through Wireshark.
 ![image](https://user-images.githubusercontent.com/85040899/120102824-4ac23a80-c166-11eb-9f03-0bdc4e64fe3b.png)


After receiving the Mac Address the chat will become encrypted.
When Server sends “hello” to Client:
 ![image](https://user-images.githubusercontent.com/85040899/120102835-557ccf80-c166-11eb-9af4-edf674a94850.png)


Wireshark sniffed information:
![image](https://user-images.githubusercontent.com/85040899/120102849-5f9ece00-c166-11eb-8f82-8b6dcfa7c356.png)
 

Same for Client Side:
When Client replied with “ hi, what’s up?” to the Server
 ![image](https://user-images.githubusercontent.com/85040899/120102858-6af1f980-c166-11eb-8774-dac664cf3145.png)


Wireshark sniffed information:
 ![image](https://user-images.githubusercontent.com/85040899/120102866-704f4400-c166-11eb-813e-737b3d5cd6a5.png)


Key Remains the Same until count of messages exchanged by Server and Client exceeds 5(excluding unencrypted messages count);i.e. in this case Server msgs=3(hello, nothing much, yes) and Client msgs=3(hi what’s up , oh okay, hello)

 i.e. count==6, the 6th message will be delivered by using the updated key which is updated by a certain formula
![image](https://user-images.githubusercontent.com/85040899/120102890-86f59b00-c166-11eb-8413-1adf6369501b.png)

 

The message sent by client on count 6 is hello, which would be encrypted by an updated key.

What WireShark Captured instead of “hello”:

 ![image](https://user-images.githubusercontent.com/85040899/120102901-9379f380-c166-11eb-87d7-122aba259654.png)

And this will be continued in the same manner for further encryption of messages.
(user can msg as many times as he/she wants to).

<h3>Let's try it on some other Computer!!</h3>
 
https://user-images.githubusercontent.com/85040899/120104373-9debbb80-c16d-11eb-873d-f977abb466d4.mp4


