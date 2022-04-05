// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

contract HelloWorld { 

        //notify the world of cool things happening (event)
        
         event NewMessage(string message); 
        //long term storage
    string public message;

       // Anyone can call the update message function
    function updateMessage(string calldata _message) public {
        message = _message;
        emit NewMessage(message);
    }
}
