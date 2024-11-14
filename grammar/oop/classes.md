/*
varName -> public variable
_varName -> protected variables variable
__varName -> private variable
*/

class MyClass {
    // public variable name
    string name = ""

    // protected variable 
    string _some_protected_var = ""

    // private variable name
    string __another_name = ""

    // static variable
    static int count = 1

    // constructor
    fn __init__(string name) {
        this.name = name
    }
}

fn (MyClass mcls) ShowInfo() {
    println(this.name)
}

fn (MyClass& mcls) ChangeVariableValue(string new_val) {
    this.__another_name = new_val
}

