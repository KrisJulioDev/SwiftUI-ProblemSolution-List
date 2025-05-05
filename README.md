**Problem**: Prevents moving the view behind when showing the keyboard

**Solution**: add ignoreSafeArea(.keyboard) to GeometryReader 
Version: Swift 6

```
GeometryReader { proxy in
    ScrollViewReader { scrollProxy in
        ScrollView(showsIndicators: false) {
            ContentOne() 
            ContentTwo()
        }
        .targetBehaviorPaging() 
    }
}
.ignoresSafeArea(.keyboard, edges: .all)    
```
