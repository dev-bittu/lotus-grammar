class MyClass {
    ...
}

class AnotherClass extends MyClass, MyClass2 {
    ...
}

// if any class implement interface then they should have the fn mentioned in that interface
// if your class not implement but have all the functions mentioned in interface then your class by default implement the interface like golang
interface Printer {
    __str__() string
}

class YetAnotherClass extends MyClass implement Printer {
    ...
}

