list mylist = ['c', "string", 12, 23.4, true, false, null, ["string", ...], {}, {"name":"bittu"}, tuple(), ("with one element",), ("string", 12)]

// add at the end of list
mylist.append(34)
>>> ['c', "string", 12, 23.4, true, false, null, ["string", ...], {}, {"name":"bittu"}, tuple(), ("with one element",), ("string", 12), 34]
mylist.append([1, 2, 3])
>>> ['c', "string", 12, 23.4, true, false, null, ["string", ...], {}, {"name":"bittu"}, tuple(), ("with one element",), ("string", 12), 34, [1, 2, 3]]
// i dont remeber what it called but it open all elements of list and pass it as argument like: mylist.append(1, 2, 3)
mylist.append([1, 2, 3]...)
>>> ['c', "string", 12, 23.4, true, false, null, ["string", ...], {}, {"name":"bittu"}, tuple(), ("with one element",), ("string", 12), 34, [1, 2, 3], 1, 2, 3]



// remove last element
mylist.pop()

// both are same
list mylist = []
OR
list<any> mylist = []

// only contains int
list<int> mylist = [1, 2, 4, 6]


difference btw array and list:
1. array have fixed size but list have not
2. 