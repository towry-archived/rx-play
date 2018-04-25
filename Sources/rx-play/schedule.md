
http://www.introtorx.com/content/v1.0.10621.0/15_SchedulingAndThreading.html

```swift
import Foundation
import RxSwift

let scheduler = MainScheduler.instance
let sampleTimer = Observable<Int>.timer(10.0, period: 10.0, scheduler: scheduler)

_ = sampleTimer.take(1).timeout(5, scheduler: scheduler).subscribe(onNext: { val in
    debugPrint(val)
}, onError: { e in
    debugPrint(e)
}, onCompleted: {
    debugPrint("onCompleted")
}, onDisposed: {
    debugPrint("disposed");
})

CFRunLoopRun()

```
