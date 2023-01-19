Q1: Who controls the ledger canister?

A1: NNS

Q2: What is the subnet of the canister with the id: mwrha-maaaa-aaaab-qabqq-cai? How much nodes are running this subnet?

A2.1: pae4o-o6dxf-xki7q-ezclx-znyd6-fnk6w-vkv5z-5lfwh-xym2i-otrrw-fqe 
A2.2: 16 nodes

Q3: I have a neuron with 1O ICPs locked with a dissolve delay of 4 years - my neuron has been locked for 2 years. What is my expected voting power?

A3: 16.86

Q4: What is wrong with the following code? actor { let n : Nat = 50; let t : Text = "Hello";
public func convert_to_text(m : Nat) : async Text { Nat.toText(m); };
}

A4.1: Need to import Nat "mo:base/Nat"
A4.2: 
import Nat "mo:base/Nat";
actor {
  let n : Nat = 50;
  let t : Text = "Hello";
  public func convert_to_text(m : Nat) : async Text {
    Nat.toText(m);
  };
}

Q5: What is wrong with the following code? actor { var languages : [var Text] = ["English", "German", "Chinese", "Japanese", "French"];

public func show_languages(language : Text) : async [var Text] { return (languages); };

}

A5.1: Need to import Array "mo:base/Array".
A5.2: Change languages array mutability to 'let' rather than 'var' and remove 'var' from the return type.
A5.3: Add 'Array.freeze' to the return array.
A5.4: 
import Array "mo:base/Array";
actor {
  let languages : [var Text] = [var "English", "German", "Chinese", "Japanese", "French"];
  public func show_languages(language: Text) : async [Text] {
    return Array.freeze(languages);
  };
}

Q6: What is wrong with the following code? actor { var languages : [Text] = ["English", "German", "Chinese", "Japanese", "French"];
public func add_language(new_language: Text) : async [Text] { languages := Array.append(languages, [new_language]); return (languages); };
}

A6: