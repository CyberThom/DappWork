# DappWork
Recording my progress of blockchain coding!
pragma solidity 0.5.1;
// people could use higher level versions of pragma that are a securit vulnerability.
contract Counter {
    uint public count = 0;

    event Increment(uint value);
    event Decrement(uint value);

    function getCount() view public returns(uint) {
    return count;
    }

    function increment() public {
      count += 1;  
      emit Increment(count);
    }

    function decrement() public {
        count -= 1;
        emit Decrement(count);
    }
}
// solidity is a stack language. You have to tell the data what type of variable is going to be stored in it.
// uint stands for an unsigned integer i.e 2. uints are always positive. 
//The numbers at the end of a unit (such as uint256) represents the amount of bits the unint can have. the size.
// by default they are 256
// The value of this variable is stored on the blockchain. Any time the value is updated it is stored on the blockchain.
// Solidity and Ethereum are event functions. Any time the increment function happens
//It will listen to the blockchain and know the count event happen.
// The event history can be tracked throught the blockchiain
// You can do this in professional contracts.
//up until line 15, we cannot call the smart contract, it doens't have visibility.
// add a public funtion.
// public tells solidity where the function can be called.
// Constructor functino
//struggled to compile because I had upper and lower cases mixed up, case sensitive.
