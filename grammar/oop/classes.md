/*
varName -> public variable
_varName -> protected variables variable
__varName -> private variable
*/

class MyClass {
    // public variable name
    let name string = ""

    // protected variable 
    let _some_protected_var string = ""

    // private variable name
    let __another_name string = ""

    // static variable
    static count int = 1

    // constructor
    fn __init__(string name) {
        this.name = name
    }
}

fn (mcls MyClass) ShowInfo() {
    println(this.name)
}

fn (mcls &MyClass) ChangeVariableValue(string new_val) {
    this.__another_name = new_val
}

