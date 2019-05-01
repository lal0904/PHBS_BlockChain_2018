#PHBS_BlockChain_2018
## The disigh of a safe crowdsourcing system based on blockchain
### BY ANLEI LIU
# 1. Introduction
In today’s fast-paced and technology-oriented society, the emergence of crowdsourcing has changed the traditional employment structure. Both employers and employees are not limited to the work contract, but the whole public in the internet. As the task requester, you can find someone with higher efficiency and talent, and also, as the worker who receive the task, can create more value and wealth with your knowledge. This process has a win-win result. Traditional crowd model is based on the third-party platform. From posting to evaluating task, every process is inseparable from the participation of the third-party. The existence of platform can bring us convenience, but it also bring us problems, like high service fee, potential hazard of information disclosure. These problems can impede the development and promotion of crowdsourcing.
In this research, we conceptualized a blockchain-based crowdsourcing framework, this decentralized system can deal with the above problems. Three smart contrasts (UC, TC, WC) can replace the working of third-platform. Two-layer system model can encrypted data and store into distribute database. Besides, we use persona to store personal information, which can reduce the information we stored in public network. Through simulation, we found that our system can maintain the basic function of original crowdsourcing system, and improve the security performance in the meantime.

# 2. Background
In the era of rapid Internet development, market competition is intensifying, and the level of knowledge owned by individuals and enterprises is difficult to meet the needs of development. Therefore, many companies choose to increase market competitiveness by acquiring external knowledge. Since Jeff Howe proposed the concept of “crowdsourcing” in 2006, this new working model quickly gained the attention of enterprises and individuals. Crowdsourcing refers to a business or organization that publishes tasks that were completed by contract signing parties on the Internet and outsources them to non-specific individuals or organizations for completion. Different from the highly specialized work mode of outsourcing, crowdsourcing emphasizes non-specificity and extensiveness. In just a few short years, the crowdsourcing platform has gradually matured. The crowdsourcing platforms that are well known in the market are mainly divided into the following categories: express delivery crowdsourcing platforms represented by Jingdong crowdsourcing, daily task crowdsourcing platforms represented by micro-defects, and IT services represented by ChinaSoft Liberation. Class crowdsourcing platform. According to the statistics released on the domestic crowdsourcing website, we found that as of the end of 2014, the number of major domestic crowdsourcing websites has exceeded 20 million, and the transaction amount is nearly 10 billion yuan. This shows that crowdsourcing has gradually penetrated into all walks of life.
The traditional crowdsourcing model generally consists of three main bodies: the issuer, the crowdsourcing platform, and the contractor. Usually, the issuer issues the tasks and requirements on the platform, and the platform matches or recommends the appropriate recipients, or the packager applies for the task. The completion of the entire task is based on a third-party crowdsourcing platform, which has some security risks. First, the personal information of the registered users of the platform, such as name, email address, telephone number, and address, are stored in the database of the crowdsourcing platform, which will expose users to risks such as information leakage. Second, the crowdsourcing service relies on the normal operation of the centralized third-party service platform. Once the platform fails, such as DDoS attacks, Single Point of Failure, etc., the entire crowdsourcing network will face embarrassment. Third, crowdsourcing services relying on third parties need to pay high service fees to third-party platforms, which also increases the extra cost of work outsourcing.

# 3. Contribution
The main contributions of this research are: (1) Constructing a decentralized crowdsourcing system based on block and blockchain, avoiding the security risks caused by untrusted third-party platforms. (2) Intelligent matching and evaluation of tasks based on smart contracts are realized, and the efficiency and accuracy in the matching process are improved, and the matching cost is also reduced. (3) A user information storage method based on "user portrait" is proposed to reduce the amount of stored information and effectively protect user privacy.

# 4. System Introduction
Aiming at the widespread popular centralized crowdsourcing system on the market, we propose a decentralized crowdsourcing system based on blockchain. In our model, there is no longer a third-party platform that may have security risks. All the links in the package, from the release of the task, the application of the applicant and the provision of personal qualifications, the signing of the work contract, the completion of the task, and the issuance of the reward, are all completed by the blockchain. Our system model is shown in Figure.
 There are three roles in our model, namely, the contractor, the contractor and the miner. The functions and functions of the different roles are introduced below.
**Requster**: The initiator of the task, you need to submit the introduction, requirements and rewards of the task in the block. Create a **task contract** (TC). At the same time as the upload task, the issuer needs to pay a certain token to pay for the miner's maintenance of the blockchain and the compensation of the contractor to complete the task.
**Receiver**: The recipient of the task can apply to complete the tasks publicized on the network. Every user on the network has its own label that records its work history. When the contractor applies to complete a job and creates a **work contract** (WC), the contract will be judged according to the label. After completing the task, the receiving party can get paid.
**Miner**: The maintainer of the blockchain, the miner adds past transaction records to the blockchain and validates a new block through a consensus agreement. They ensure the normal operation of the blockchain and earn mining and mining rewards by solving mathematical problems. Each user in the system can play the role of a miner, participating in and getting paid when the computer is rich in computing power.

# 5. System architecture
In this part, we will introduce the logical layer and data layer in this system in turn. The logical layer consists of a blockchain network that provides an environment for the operation of smart contracts and also provides an operational interface for the user. The data layer is used to store raw data, save the results of tasks, and so on.
### 5.1  Blockchain logic layer
The logical layer is also the blockchain layer, which is based on the user interaction and data processing layer of the blockchain network. This layer serves two main purposes. One is to use the consensus mechanism in the blockchain network to identify and execute each step. The confirmation of each node can maintain the system's self-trust mechanism, and the second is to execute the smart contract. The miners in the blockchain can complete the task by mining the contract nodes. In addition to storing smart contracts, the block also stores the metadata of the original data in the data storage layer, including the owner number, timestamp, pointer to the location where the data is stored, and data such as hash values. With this data, users only need to verify that the metadata is intact to prove the security and integrity of the data storage layer data.
### 5.2 Data Storage Layer
   As the bottom-level data storage module of the system, the storage layer stores the real data of tasks and solutions. When the sending party issues a task, it signs the data with a private key and stores the task requirements in a distributed database. When the receiver completes the task, it also uploads the task to the distributed database, signing with his private key, the smart contract will use its public key for authentication, and the task solution will be encrypted with the public key of the issuer. Only after the sender has verified the data integrity, the private key can be used to obtain the solution stored in the database, and no one else can decrypt and obtain the relevant data. This method of storing data separately can greatly expand the storage capacity of our system and make rational use of storage space.

# 6.  Smart Contract Design
The smart contract in this system consists of the following three contracts: User Contract (UC), Task Contract (TC) and Work Contract (WC). When the user first uses it, it needs to register in the blockchain, and at the same time generate a user contract. The user contract will assign a pair of public and private keys to the user for encryption and signature in the data storage process. When the issuer issues a task, first create a task contract for the task, and encrypt the original data of the task in the data storage layer. The task contract will complete the broadcast and matching process of the task. After the matching is completed, the work contract will be activated, the solution submitted by the docking party will be checked, the image will be updated for the user, and the reward will be distributed.
### 6.1 User Contract (UC)
A user contract is a smart contract created at the beginning of each new user registration, primarily for identity and key assignment. When the user applies, there is no need to provide a real identity. The system will assign the user a pseudonym (user ID) and a key pair: a public key and a private key. In the entire system, a user address is generated by hashing the user's public key, which is used to store the user's personal information. Here, personal information refers to the user's portrait and pseudonym. This approach allows users to get a specific user ID without submitting real personal information. At work, users post and apply for tasks under pseudonyms. In the user contract, it also contains a preliminary depiction of the user's portrait. When registering, the user can select some types of jobs that can be qualified according to the task classification, and get the original task history. This can ensure that the related tasks can be broadcast to the new registration during the subsequent task delivery. Users, users also need to pay a certain fee when registering, used to reward miners in contract creation.
### 6.2 Task Contract (TC)
The task contract is a smart contract created when the issuing party issues a task. The main task is to direct the broadcast task according to the requirements of the issuer, and select the better assignment task from the applicant. The information contained in the contract includes the location where the task is stored in the data storage layer, the ID of the issuer, the requirements of the issuer for the task, and the cost of executing the contract. The execution of the contract relies on the miner's mining work in the blockchain network. Once the contract is executed, it will automatically push the task-related requirements to the qualified users according to the requirements of the contractor and process the applicant's application information. When applying for a task, the applicant needs to deposit a certain amount of deposit in the contract to ensure the smooth progress of the work. This fee will be refunded to the receiving party after the task is completed and passed. For the matching method of personnel, we have described in detail in the previous chapter how the system screens according to the user's portrait, so I won't go into details here. When the task contract completes the user matching process, the parameters are passed to the work contract (WC). At this point, the work of the task contract is completed, and the execution node can get the fee for completing the contract.
### 6.3 Work Contract (WC)
A work contract is a smart contract that is generated after the task is successfully released and received. It is mainly responsible for supervising the completion of the task and assigning rewards. After the task contract filters the recipient according to the requirements of the issuer, the task contract transmits the issuer and the recipient ID, the task related information, and the task reward and margin to the work contract, and activates the smart contract. Since the blockchain storage space is limited, when the issuer completes the task, the solution is uploaded to the data storage layer for storage, and the feedback is submitted to the work contract. In traditional crowdsourcing systems, the assessment of the solution is done directly by a third-party platform or the contractor. In our system, the work contract will be evaluated in place of the third-party platform. We set up an evaluation function Assess( ). The specific evaluation indicators are determined by the contractor and then completed by the miners in the blockchain. Since the solution is stored in the data storage layer by the public key of the issuer, the contract execution node cannot directly obtain the real content, and the initial judgment can be performed by using the homomorphic encryption method, but how to evaluate the solution in the encrypted state. This is also one of the problems we have to solve in the future. At present, our proposed system can judge some simple indicators, such as time and place. When the work contract is detected, the test result is fed back to the issuer, prompting the issuer to extract the solution. After the result is verified, the contractor returns the result to the work contract WC. The contract updates the user image of the issuer according to the feedback result, passes the new parameter to the user contract UC, and issues the task reward to the receiver, ending the present. jobs
 
 # 7. Work Process
### 7.1 User registration
When a new user first uses the system, the registration step will be completed. The main purpose of the registration step is to create a User Contract (UC), which will create a portrait for the user for the first time, stored in the node along with the user-assigned pseudonym. Users can select certain labels according to their own skills to facilitate the push of tasks. This operation is used as a startup step of the recommendation algorithm. When there is a related task, even if the related task is not completed in the new user history, the related task can be received. Regardless of whether it is an issuer or a package, the user registration step cannot be omitted.
### 7.2 Task creation
When the contractor needs to release the task, first submit the task related requirements and auditing standards, and store a certain token into the blockchain, as a reward for completing the task and maintaining the cost of the blockchain. At the same time as the task is submitted, a task contract (TC), a pointer to store the task, and the like are generated and compiled into an executable task release code and a personnel screening code.
### 7.3 Task release
After the task stores and generates the task contract (TC), the miner in the blockchain will execute the task release code in the contract, find the user with the relevant tag according to the image of the retrieved user node, and deliver the task information. This is a directed broadcast process in which only users with relevant requirements receive task messages.
### 7.4  Personnel matching
When a node receives and applies for a task, it will respond to the notification initiated by the task contract (TC). According to the applicant's situation, the TC will perform the personnel screening code to judge the applicant's portrait, according to the relevant work. And score, according to the requirements of the contractor to filter, select the outbound party, and pass the parameters of the task and the contractor to the task partners to build a work contract (WC).
### 7.5 Submit a proposal
After the contractor completes the work task, upload the solution to the distributed database and encrypt it with the public key of the issuer. And feedback to the work contract (WC), the smart contract according to the requirements of the contractor, the initial assessment of the solution, such as whether to submit according to the specified time. If the requirements are met, the results are fed back to the issuer, prompting the issuer to check the task.
### 7.6 Evaluation and reward
For tasks with more complex results, the contractor needs to extract the data before judging the pros and cons of the solution. After the package party decrypts the solution through the private key, it gives a feedback to the work contract (WC), which includes the task completion score. After receiving the feedback, the work contract re-modifies the user image of the recipient according to the work situation and adds new The work record and the distribution of rewards based on the completion status.
A complete crowdsourcing task generally covers the above six aspects. When both the sending party and the receiving party are old users, step one can be omitted, starting directly from step two.
 
# 8 . Algorithm Design
### 8.1 User registration
When a new user joins the blockchain crowdsourcing system, it is necessary to register an account and create a user contract (UC). The variables input in the algorithm 1 have a user-defined pseudonym Uid, the user pseudonym stores the pool Pool, the user registration state rgt, and the user skill is represented by the number i, and the user skill is an important component of the user portrait pic. When the user registers, if the test is a new user, the contract will use the generate() function to assign a pair of keys Kp and Ks to the user. The user's address is hashed by the hash() function to the user public key Kp. For storing user information. After the user has their own address, Uadr, the picture() function will first generate an image for the user. At this point, the registration is complete. The specific algorithm is described as follows:

***Input**: user ID: Uid, user pool: Pool, user skills: Skill i, 
**Output**: user address: Uadr, public key: Kp, private key: Ks, Register: rgt, *
```html
user’s picture: pic
rgt= false;
if Uid in Pool 
  goto finish;
Ks,Kp= generate(Uid);  //generate keys for user
Uadr= hash(Kp); //use the hash value as the address of the user
Pic= picture(skill i); 
Rgt= ture;
Finish;
Reture pic, rgt, Uadr
```

### 8.2 Publishing tasks
When the issuer issues a task, a task contract (TC) is created, the relevant information of the task is stored in the data storage layer, and the contract is used for personnel matching. We set the following variables: task specific content and description Rq, applicant minimum completion of related tasks Tmin, minimum average score Savgmin, latest submission time Tfin, and expected number of recipients Num. This information is used to describe the requirements of the task and to assist in the screening and matching of the contract personnel. When the contractor issues a task, it needs to deposit a certain amount of reward in the blockchain in advance, as work compensation and fuel costs. The input task description Rq will be stored in the data storage layer using the encrypt() function and generated using the point() function and the hash() function to generate the pointer PoT and the hash value Ht. After the above steps, the task successfully encrypts the storage and generates key information.
After the task storage is completed, the release of the task and the matching of the personnel will be performed. We define a function broadcast that retrieves all users who have i tags and pushes task information to them. For the users who apply, we number them Wj and compare their indicators. The user who applied for the task needs to pay a certain amount of margin bond. We have defined the minimum margin BOND in the system, and only the amount of the payment exceeds the minimum amount to apply for the task. For applicants with successful contract matching, the inform() function will be used to notify the issuer. This section uses a first-come, first-served screening method to assign tasks according to the order of the applicants. The distribution algorithm will be improved in the future, taking into account the applicant's work experience and the amount of the deposit.
After the task is published and matched, the task contract ends, returning the task pointer and the recipient information, passing the parameters to the work contract, and activating the new task contract.

***Input**: requester ID: Uid(R), rgt(R),
   Requirements: description of the task: Rq
Type of task: i 
Times of finished related job: Tmin； Lowest average mark: Savgmin； Expected finish time: Tfin；Expected number of wokers: Num； reward
**Output**: point of task: PoT
  Hash value of task: Ht
  Workers id: Uid(Wj), Worker address: Uadr(Wj) Bond(Wj)*
```html
If rgt(R)= false
  Goto finish;
Lock(reward); //save the reward on the blockchian
Rq’= encrypt(Rq, Ks(R))；
PoT= point(Rq’); // save the row data of requirements into storage layer
Ht= hash(Rq’); // create the hash value of task
Broadcast (i); // broadcast the task to all user with the label i
If Savgij>= Savgmin
  If Tij>= T min
If bond(j)>= BOND // the worker pay enough bond
  { Inform(Uadr(Wj)); //inform j that he got the job
     If j>= Num
       Goto finsh;}
Else goto finish；
finish；
Return Uadr(Wj), Uid(Wj), Bond(j), PoT, Tfin；
```
### 8.3 Task execution and feedback
After obtaining the parameters passed by the task contract, the work contract (WC) will be activated, and the task contract will pass the information of the issuer and the receiver and the task-related parameters to the work contract template to generate a new work contract. The work contract is mainly responsible for urging the contractor to complete the work on time, and feedback the solution to the issuer to modify the user image of the acceptor according to the evaluation given by the issuer. In this section we define the new variable Sol, which is used to store the solution for the task.
At the beginning of the work contract, the receiver uses PoT to extract the task details through the get() function. When the task is completed, the contract will first check if the result is submitted within the specified time, and if it times out, exit the program directly. The solution's storage also uses encryption and signature techniques, which are processed in the data storage layer using the encrypt() and signature() functions, respectively. After the upload is completed, the contract will notify the contractor to accept. During the acceptance process, the sending party first uses the address pointer PoS to find the storage location, uses the public key of the receiving party to perform signature verification, and then uses its own private key to decrypt. This process is done by the verify() function.
After the verification, the contractor will feedback a task score Sij to the smart contract. As the evaluation of this task, the contract will automatically update the user portrait, unlock the deposit of the contractor, and issue the reward. At this point, a complete workflow ends.

***Input**: Expected finish time: Tfin, point of task: PoT, requester ID: Uid(R), worker ID: Uid(Wj), bond(Wj)
**Output**: point of solution: PoS；Hash value of solution: Hs *
```html
Lock(bond(Wj));
get(PoT); // worker get the task for storage layer
if now>= Tfin // time is out
  goto final;
Sol’= encrypt(Sol, Kp(R); // Sol is the raw data of solution
Sol’’= signature(Sol’, Ks(Wj));
PoS= point(Sol’’);
Inform(Uadr(R)); inform the requester that worker has already submitted solution.
Sij=verify(PoS, Kp(Wj), Ks(R)); // the requester verify the signature and the solution, and give a point Sij
Update(pic(Wj), Sij); //update the user picture of Wj
Unlock (bond(Wj));
Unlock (reward);
Distribute(reward);
Finish；
Return 0；
```
![markdown]
(https://github.com/lal0904/PHBS_BlockChain_2018/blob/master/算法.png)

# 9. Conclusion
In this research, we propose a blockchain-based secure crowdsourcing system. This is a crowdsourcing system that does not rely on third-party platforms and can effectively protect users' privacy. With the help of technologies such as decentralization, consensus mechanism and executable intelligent contract in the blockchain network, problems such as high service cost, possible leakage of user privacy and vulnerability of centralized data storage in the existing crowdsourcing system can be solved. This system starts from the characteristic of decentralization and tries to replace and improve the traditional mode. In the absence of a third party platform, it is necessary to solve the problems of task release, personnel matching and work verification. To solve the above problems, we use smart contracts that can be automatically executed in the blockchain to replace the original third-party work. Users only need to pay for the maintenance of the blockchain, which can also reduce costs. In the design of workflow, we retain all the functions of the original crowdsourcing system, and on this basis, we propose a user privacy protection scheme to minimize the historical data saved by users in the network. This system stores the user information with the false name and the user portrait, even if the database is attacked, also cannot match the above data with the real identity. Through simulation test, we find that the decentralized crowdsourcing system proposed in this paper can maintain the original crowdsourcing function and successfully compress the user information.

The main work of this research is as follows:

(1) a two-layer system model is proposed, which is the block chain logic layer and the data storage layer respectively. Data encryption is stored in the distributed database, and only variables such as pointer, time stamp and hash value are stored in the block, greatly increasing the system capacity. To realize the distributed storage of data, users do not need to trust the third-party storage server.

(2) three smart contracts are designed to replace the work of traditional third-party crowdsourcing platforms. The three contracts are user contract, task contract and work contract. Work when a user registers, publishes a task, and completes a task, respectively.

(3) the concept of "user portrait" is adopted to store user information and hide real information and historical data. While not affecting the work matching, the information stored by users is reduced to the maximum extent to avoid the hidden danger caused by data leakage.

(4) a complete workflow is provided and the algorithm is designed. The reliability of the system is proved by simulation.


