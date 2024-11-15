fn PrintHelloWorld() {
    print("Hello World!")
}

fn PrintAllElementOfList(lst list) {
    for (element in lst) {
        print(element)
    }
}

fn PrintAllElementOfDict(dct dict) {
    for (element in dct) {
        print(element, dct[element])
    }

    /* or we can do that
    for (element, value in dct.items()) {
        print(element, value)
    }

    lets say we have a dict:
    let mydict dict = {"name": "bittu", "myfavchar": 'b', "favnum": 7}
    then output of mydict.items() it this:
    (("name", "bittu"), ("myfavchar", 'b'), ("favnum", 7))
    while iterating if we use one variable to hold the element then element will look like:
    ("name", "bittu")
    ("myfavchar", 'b')
    ("favnum", 7)

    thats why we use tuple unpacking for this.
    */
}

fn main() {
    PrintHelloWorld()
    PrintAllElementOfList([
        "string", 
        14,
        1.4,
        true,
        null,
        'a',
        ["hfg", 2, 5.6]
    ])
}