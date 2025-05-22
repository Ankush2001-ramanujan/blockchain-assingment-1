# blockchain-assingment-1



#Create Metamask Wallet (Sepolia Testnet)


#Introduction
1.Network : Sepolia Testent

2.Amount Sent : 0.02 ETH


4.Status : Successful


#Getting Sepolia ETH from Faucet

1.Visited the google cloud Sepolia Faucet.

2.Logged in with my google account.

3.Entered my Metamask wallet address.

4.Clicked on "Request 0.02 ETH".

5.ETH was sent to my wallet within a few seconds.

6.Verified the transaction on sepolia Etherscan.



#STEPS FOLLOWED

1.Connected Metamask to Sepolia Testnet.

2.Claimed Sepolia ETH from faucet.

3.Sent ETH to another Address

4.Verified transaction was confirmed.

#screenshot

below is the screenshot of the transaction


![WhatsApp Image 2025-04-21 at 11 17 40_bdd5b73a](https://github.com/user-attachments/assets/b414ef4a-dd32-4544-90ac-f6c8c7215e58)


![WhatsApp Image 2025-04-21 at 11 17 40_323e7cd5](https://github.com/user-attachments/assets/681641fb-d19f-4a25-a293-f8ec8f8ea40d)


#Practical 2


#IPFS Practical - Uploading a file to IPFS
#IPFS Installation

 downloaded and install IPFS desktop for windows from the official website : https://docs.ipfs.tech/install/ipfs-desktop/
 #IPFS Setup
 
After installing, I launched the IPFS desktop.
IPFS node automatically connected and status showed as Online.

#File Upload
1.I clicked on the file section in IPFS Desktop.

2.Then i selected the option "Import" and uploaded a sample file, picture of flower and music also.

3.Once the file was uploaded, IPFS generate a unique CID(Content Identifier) for the file.

![Screenshot 2025-04-10 113433](https://github.com/user-attachments/assets/c614dc6b-b154-48e2-b1d6-a1ff16c5a302)

#Encrypting and Decrypting

1.Download IPFS CLI:
wget ```https://dist.ipfs.tech/go-ipfs/v0.22.0/go-ipfs_v0.22.0_linux-amd64.tar.gz```

2.Extract the tar file:

```tar -xvzf go-ipfs_v0.22.0_linux-amd64.tar.gz```

3.Install IPFS:

```cd go-ipfs```

```./install.sh```

4.Initialize IPFS Node

```~/.local/bin/ipfs init```

5.Start IPFS Daemon

```~/.local/bin/ipfs daemon```

6.Create a sample file

```echo "hello, IPFS!" > hello.txt```

6.Add original file to IPFS

```~/.local/bin/ipfs add hello.txt```

7.Encrypt the file using OpenSSL

```openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in hello.txt -out hello.enc```

8.Upload the encrypted file to IPFS

```~/.local/bin/ipfs add hello.enc```

9.Decrypt the file

```openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in retrieved.enc -out decrypted.txt```

10.See decrypted content

```cat decrypted.txt```

11.Add decrypted file to IPFS

```~/.local/bin/ipfs add decrypted.txt```



#Practical 3


#Hyperledger Fabric Practical

1.Install Golang

```sudo apt install golang-go```


#Screenshot

![WhatsApp Image 2025-04-21 at 11 44 11_058135ab](https://github.com/user-attachments/assets/4fca1426-473f-45a1-a859-1db486e60aaa)



2.Check Docker Version

```docker --version```

Verifies that Docker is installed and running correctly.

#screenshot

![WhatsApp Image 2025-04-21 at 11 44 11_460f8bb6](https://github.com/user-attachments/assets/1a0ae3f6-0108-4baa-8af5-3fe21936b443)



3.Check Docker Compose Version

```docker compose version```

Verifies the installation of Docker Compose.

#screenshot

![WhatsApp Image 2025-04-21 at 11 52 25_2718e33c](https://github.com/user-attachments/assets/c638e357-5c37-4be4-a1c3-d4035c6c3498)



4.List Files in Current Directory
```ls```

Shows the list of files and folders in the current directory.


5.Clone the Fabric Samples Repository and Move into the Cloned Folder

```git clone https://github.com/Akshitakaushik123/fabric-samples.git; cd fabric-samples```

Downloads the official Hyperledger Fabric sample code from GitHub. Enters the cloned folder where Fabric examples are available.


#screenshot


![WhatsApp Image 2025-04-21 at 11 44 12_3dffbe75](https://github.com/user-attachments/assets/2b8eab1f-f696-4500-a1a5-8e8fe6f4022b)



6.Download Fabric Binaries

```curl -sSL https://bit.ly/2ysbOFE | bash -s```

Downloads necessary Fabric binaries and Docker images like peer, orderer, and cryptogen.

#Screenshot

![WhatsApp Image 2025-04-21 at 11 44 12_70ddd487](https://github.com/user-attachments/assets/2a816bc6-c0b1-4947-9ecd-d1370366ab7a)


![WhatsApp Image 2025-04-21 at 11 44 13_29da4bcc](https://github.com/user-attachments/assets/f9192bff-2b77-4167-98cf-2f4fa3114cdc)



7.Enter the Test Network Directory

```cd test-network```

Navigates to the directory that contains scripts for running a sample Fabric network.


#Screenshot

![WhatsApp Image 2025-04-21 at 12 00 08_29f54d96](https://github.com/user-attachments/assets/fc2c7480-6026-4a73-a4c8-be8ee2dfa8e6)



8.View the Network Script

```./network.sh```

Shows the options available with the network.sh script.

#Screenshot

![WhatsApp Image 2025-04-21 at 11 44 13_d042df86](https://github.com/user-attachments/assets/efb2d661-8706-4330-bef5-f53326442be4)



9.Start the Fabric Network

```./network.sh up```

Starts the network by launching peer, orderer, and CA containers, and generates the required cryptographic materials.

#Screenshot

![WhatsApp Image 2025-04-21 at 11 44 14_eb5ca2fd](https://github.com/user-attachments/assets/fca12f83-5504-406e-8b35-6e64fe8f19ad)



10.Create a Channel

```./network.sh createChannel```

Creates a default channel (usually named mychannel) and joins the peers to it.


#Screenshot



11.Shut Down the Network


```./network.sh down```

Stops all containers and deletes the crypto material and artifacts created during the setup.

#Screenshot


![WhatsApp Image 2025-04-21 at 11 44 15_4b7926cd](https://github.com/user-attachments/assets/7ed34dbf-0f3f-431f-98ab-eb84ef12202d)



#Practical 4


Solidity
Step 1: Set Up the Development Environment


Website: https://remix.ethereum.org

It’s an online editor where you can write, test, and deploy Solidity code directly in your browser. No installation needed.


Step 2: Write Your First Smart Contract (in Solidity)

pragma solidity ^0.8.0;

contract HelloWorld {
    string public message = "Hello Blockchain!";

    function setMessage(string memory newMessage) public {
        message = newMessage;
    }
}

#Step 3: Compile the Contract In Remix:


Click on the Solidity compiler tab (compiler icon).


Click Compile to check for errors.



![Screenshot 2025-05-15 235325](https://github.com/user-attachments/assets/4a1a252a-bb87-4e29-b14f-142897bb20f9)




#Step 4: Deploy the Smart Contract Go to the Deploy & Run Transactions tab in Remix.

Choose Environment as "JavaScript VM" (for testing in browser).

Click Deploy.

After deployment, contract will appear in the Deployed Contracts section.

Step 5: Interact with the Contract Now you can:

Click message() to read the current message.

Use setMessage() to change the message.

This simulates how smart contracts work on blockchain.


#  sec-practical-
## Create a voting system with multiple candidates. Each address can vote only once.
```
pragma solidity ^0.8.0;

contract Voting {
    struct Candidate {
        string name;
        uint voteCount;
    }

    Candidate[] public candidates;
    mapping(address => bool) public hasVoted;

    constructor(string[] memory candidateNames) {
        for (uint i = 0; i < candidateNames.length; i++) {
            candidates.push(Candidate(candidateNames[i], 0));
        }
    }

    function vote(uint candidateIndex) public {
        require(!hasVoted[msg.sender], "You have already voted");
        require(candidateIndex < candidates.length, "Invalid candidate index");

        candidates[candidateIndex].voteCount++;
        hasVoted[msg.sender] = true;
    }

    function getCandidates() public view returns (Candidate[] memory) {
        return candidates;
    }

    function totalCandidates() public view returns (uint) {
        return candidates.length;
    }
}
```
![image](https://github.com/user-attachments/assets/3ca00e3f-5ef9-47b8-ac4f-0dfe12202604)
![image](https://github.com/user-attachments/assets/a3d22f46-14e2-4b16-9c42-8445dd170215)


## Write a contract that manages a list of student records (name, roll number). Allow adding and retrieving student data.
```
pragma solidity ^0.8.0;

contract StudentRecords {
    struct Student {
        string name;
        uint rollNumber;
    }

    Student[] public students;

    function addStudent(string memory _name, uint _rollNumber) public {
        students.push(Student(_name, _rollNumber));
    }

    function getStudent(uint index) public view returns (string memory, uint) {
        require(index < students.length, "Invalid index");
        Student memory s = students[index];
        return (s.name, s.rollNumber);
    }

    function totalStudents() public view returns (uint) {
        return students.length;
    }
}
```
![image](https://github.com/user-attachments/assets/414c9b03-d58f-46c8-a829-d338a10deb3d)
![image](https://github.com/user-attachments/assets/33c2639e-8690-4a9d-8e27-6b7b12c93aba)


## Develop a contract that only allows the deployer (owner) to call a specific function (use modifiers).
```
pragma solidity ^0.8.0;

contract OwnerOnly {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Not the contract owner");
        _;
    }

    function privilegedAction() public onlyOwner {
        // Protected logic here
    }
}
```
![image](https://github.com/user-attachments/assets/d59c7cb4-d0ba-412b-b3ac-24e7f2a75eee)
![image](https://github.com/user-attachments/assets/39f24ed2-33b4-4651-a3e4-bc7c6494fd90)



## Write a contract where people can donate Ether and the top 3 donors are tracked
```
pragma solidity ^0.8.0;

contract TopDonors {
    struct Donor {
        address addr;
        uint amount;
    }

    Donor[3] public topDonors;

    function donate() public payable {
        require(msg.value > 0, "Must donate some ETH");

        // Check if already a top donor
        for (uint i = 0; i < 3; i++) {
            if (topDonors[i].addr == msg.sender) {
                topDonors[i].amount += msg.value;
                sortTopDonors();
                return;
            }
        }

        // Replace the lowest if new donor is bigger
        if (msg.value > topDonors[2].amount) {
            topDonors[2] = Donor(msg.sender, msg.value);
            sortTopDonors();
        }
    }

    function sortTopDonors() internal {
        for (uint i = 0; i < 3; i++) {
            for (uint j = i + 1; j < 3; j++) {
                if (topDonors[j].amount > topDonors[i].amount) {
                    Donor memory temp = topDonors[i];
                    topDonors[i] = topDonors[j];
                    topDonors[j] = temp;
                }
            }
        }
    }

    function getTopDonors() public view returns (Donor[3] memory) {
        return topDonors;
    }
}
```
![image](https://github.com/user-attachments/assets/3e07eb74-cbc6-4af6-bc49-23dd21e10b63)
![image](https://github.com/user-attachments/assets/a054973c-9941-48af-87ee-1e198f5b3a4b)


## Implement a simple auction system where users can place bids, and the highest bidder wins.
```
pragma solidity ^0.8.0;

contract SimpleAuction {
    address public highestBidder;
    uint public highestBid;
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function bid() public payable {
        require(msg.value > highestBid, "Bid too low");

        // Refund previous bidder
        if (highestBid > 0) {
            payable(highestBidder).transfer(highestBid);
        }

        highestBidder = msg.sender;
        highestBid = msg.value;
    }

    function endAuction() public {
        require(msg.sender == owner, "Only owner can end auction");
        payable(owner).transfer(address(this).balance);
    }
}
```
![image](https://github.com/user-attachments/assets/e713b9ad-cf8a-4297-8ae8-7c12080ec553)
![image](https://github.com/user-attachments/assets/2f1e35bf-9459-450f-913c-6519c78b1ac8)


## Create a contract that splits incoming Ether between 3 fixed addresses.
```pragma solidity ^0.8.0;

contract EtherSplitter {
    address payable public addr1;
    address payable public addr2;
    address payable public addr3;

    constructor(address payable _a1, address payable _a2, address payable _a3) {
        addr1 = _a1;
        addr2 = _a2;
        addr3 = _a3;
    }

    receive() external payable {
        uint share = msg.value / 3;
        addr1.transfer(share);
        addr2.transfer(share);
        addr3.transfer(msg.value - 2 * share); // Handle rounding
    }
}
```
![image](https://github.com/user-attachments/assets/dae8c819-6eae-444b-9ca9-052a6060fe08)
![image](https://github.com/user-attachments/assets/b43626ea-c669-4dc4-a5bb-0bc41226b59f)











