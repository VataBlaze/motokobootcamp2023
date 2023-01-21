Q1: Is the heap memory saved when upgrading a canister? How much heap memory does a canister has?

A1.1: No
A1.2: 4GiB

Q2: How much accounts can a unique Principal own?

A2: 4,294,967,295

Q3: Can we safely upgrade a canister from interface A to interface B?

Interface A
actor { public func greet(surname : Text, firstname : Text) : async Text {
    return "Hello" # firstname # surname # " !"; }; }

Interface B
actor { public func greet(firstname : Text) : async Text {
    return "Hello" # firstname # " !"; }; }

A3: Yes