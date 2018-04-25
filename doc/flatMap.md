```swift
_ = Observable.from([1,2,3,4,5])
  .flatMap {
    return Observable.just($0)
  }
  .subscribe(onNext: {r in
    print(r)
  }, onCompleted: {
    print("completed")
  })
```
