fn PrintLine() {
    print("Hello World!")
}

// fn returning int
fn PrintLine() int {
    print("Hello World!")
    return 0;
}

// fn returning multiple values
fn PrintLine() (int, int) {
    print("Hello World!")
    return 0, 1;
}

// anonymous fn
fn() {
    ...
}

// fn with default value
fn addTwoNum(int num1, int num2 = 5) int {
    return num1+num2
}