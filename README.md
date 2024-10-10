
contract MyNewToken {

    // public variables here
    string public tokenName = "Dickson Vecina";
    string public tokenAbbrv = "DV";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }

}

4.Compile and run the project

5.Deploy the project

Note: If 0.8.26 version is having issues for you, try using other versions.

Author

Dickson Vecina

202110060@fit.edu.ph
