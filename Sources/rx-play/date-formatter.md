```swift
import Foundation

let now = Date()
let dateFormatter = DateFormatter()
dateFormatter.dateStyle = .short
dateFormatter.timeStyle = .long
dateFormatter.dateFormat = DateFormatter.dateFormat(fromTemplate: "EEEE", options: 0, locale: Locale.autoupdatingCurrent)

let formattedNow = dateFormatter.string(from: now)
print(formattedNow)
```
