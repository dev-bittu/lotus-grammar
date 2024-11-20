
// break is used by default if you want to fallthrough then use keyword fallthrough
switch ("monday") {
    case "moday":
        print("its monday")
    case "tuesday":
        print("its tuesday")
    ...
    default:
        print("you choose wrong option")
}

OR use with enum

enum Day {
    MONDAY = 0,
    TUESDAY,
    WEDNESDAY,
    ...
}

case (MONDAY) {
    case MONDAY:
        print("its monday")
    case TUESDAY:
        print("its tuesday")
    ...
    default:
        print("you choose wrong option")
}