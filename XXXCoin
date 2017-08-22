pragma solidity ^0.4.11;

import "./StandardToken.sol";
import "./Ownable.sol";


/**
 *  XXXCoin token contract. Implements
 */
contract XXXCoin is StandardToken, Ownable {
  string public constant name = "XXXCoin";
  string public constant symbol = "XXX";
  uint public constant decimals = 4;


  // Constructor
  function SkinCoin() {
      totalSupply = 100000000000;
      balances[msg.sender] = totalSupply; // Send all tokens to owner
  }

  /**
   *  Burn away the specified amount of XXXCoin tokens
   */
  function burn(uint _value) onlyOwner returns (bool) {
    balances[msg.sender] = balances[msg.sender].sub(_value);
    totalSupply = totalSupply.sub(_value);
    Transfer(msg.sender, 0x0, _value);
    return true;
  }

}
