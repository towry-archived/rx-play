protocol pOne {
    // test: try comment bottom.
    func hello()
}

extension pOne {
    func hello() {
        print("hello")
    }
}

struct A: pOne {
    func hello() {
        print("a")
    }
}
