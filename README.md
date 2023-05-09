## RafidulIslam_Smartcontract2
### Array and structure

Here we have created Array and structure<br>
Structure means we are creating new data type.<br>
Array is a data structure that will store large amount of data of same type.<br>


```
//SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract rafiSimplestorage {
  // basic data types: boolean, uint,int,address,bytes
  //uint(unsigned integer only positive),int both pos and neg
  //address is the address of the account
  //string are secretly byte objects only for text
  //bytes32 is a bytes objects whre 32 represent how many bytes we want them to be,max size is 32
  //byte objects look like 0xsdsysydggt
  //unint256 here 256 is bit (8,16,32 upto 256 we can use)
  uint256 goodNumber;//remove public so that we don't get duplicate functions at the moment we will just get the retrieve function
   //if we have whole bunch of variables inside the contract rafiSimplestorage those actually get indexed
   //here 'uint256 goodNumber' will get index to 'zero'
 
//Below we have created a new type in our solidity that holds both good number and name
  struct Person{
    uint256 goodNumber;//this get indexed to 0
    string name;// this get indexexd to 1
//whenever we have list of variables inside an object they automatically get indexed

}

  // here below we create an array of uint256 and now good number can be a list or array
  //uint256[] public goodNumbersList;

//here below we want an array of Person we give it visibility of public and variable name person
  Person[] public person; //it is automatically giving a view function and it will give nothing if it is empty and in it's button the value that it wants is gonna be the index of the object
// array above is a dynamic array because size of the array is not given at it's initialization if we don't add any size it can be any size and here we gonna work with dynamic array

//pasing parameter of type uint256 and made the function public
  function store(uint256 _goodNumber) public{
      goodNumber = _goodNumber;
   
  }

  function retrieve() public view returns(uint256){
    return goodNumber;
  }

  //now we will create a function that is going to add Person to person array
  function addCustomer(string memory _name, uint256 _goodNumber) public {
     
      individuals.push(Person(_goodNumber,_name));//Here we have created a push function which is available in our Person object
      //Here in the above inside the push function we have created a new Person object that will take good number and name.
  //push Person in our person array ,we can also do in this way
  }


 
}


```


![rafi](https://github.com/MdRafidulIslam/rafi-smart-contract2/assets/86659473/0f5a37c0-ba80-4cc8-bcf9-2f650fd1d747)


<br><br>
