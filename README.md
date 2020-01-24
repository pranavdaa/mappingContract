# mappingContract

pragma solidity ^0.5.12;

contract MyContract {
    uint private peopleCount = 0;
    mapping(uint => Person) public people; 
     
    struct Person {
        string f_name;
        string l_name;
    }
    
    function addName(string memory f_name,string memory l_name) public {
    peopleCount += 1;
        people[peopleCount] = Person(f_name,l_name);
    }
}
