
import Foundation

class PrintableStruct : NSObject {
    public override var description: String {
        return "This is PrintableStruct"
    }
}

// extension PrintableStruct : Equatable {
//     static func == (lhs: PrintableStruct, rhs: PrintableStruct) -> Bool {
//         return true
//     }
// }

func subscribe<O: Equatable>(_ name: O) {
    print(name)
}

let ps = PrintableStruct()

subscribe(ps)
