how to export variable:
let (
    some_var = 23  // public var
    _some_var = 23  // private var
    some_another_var = 435
)

const (
    CONST_VAR = "dfgdf"  // public onst
    _CONST_VAR = "dfgdf"  // private onst
    PI = 3.14
)



every var is public, and var which start with _ is private means it not export from package (only accessible within package)
same rule applied for classes, func, interface and allother things

we not encourage you to use _ for var/func/classes defination, instead you can specify what you export or what to not export in a special file named `pkg.b2` which is present (should) in every package and this is similar to __init__.py in python.

here you can manually declare, which var is to be excluded from exporting or included. at a time you can only specify inlude which or exclude what, you cant use both in a package. 

var/func/classes defination have more priority than pkg.b2
means you you declare with prefix _ that means it will become private and not exported even if add that in include in pkg.b2



