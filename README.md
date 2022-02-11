## Configuration Steps:

```
1. From Xcode 5 we can add svgs files as the assets.
2. In order to make use of svg icon , select preserve vector data at the right sidebar
3. Import app icons at the desired directory , by making use of right click, open the folder in finder and placing all icons and contents.json
4. Select New Folder from selection option at the context menu and place other icons as well.
5. Select + icon at the bottom left corner ( where the assets are placed ) and choose color set
6. Choose Both ( Any Appearance + Dark ) Cards at the Color Set Panel. Pick 8-bit Hexadecimal at the input 
method and type desired hexcode.
7. Drag and drop the color set files as well at the Assets.xcassets
```

## Accent Color (buttons, navigation items):

```
It's a new dedicated color set created by default since xcode 12. It will be globally used by the OS in ios 14 app.
AccentColor => Appearance -> Any Dark => Content => SRGB Color System
```

## Basic Structure Of ContentView :

```
import SwiftUI
struct ContentView: View {
    var body: some View {
        Text("Hello, world!")
            .padding()
    }
}
struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```

## NOTE

```
cmd + click to wrap components inside other components
```

## CardView

```
Right Click the View Group And Select New File. Select SwiftUIView and click on the next button. 
```

## Show/Hide Preview

```
option + command + enter
```


## ZStack

```
SwiftUI has a dedicated stack type for creating overlapping content, which is useful if you want to place some text over a picture for example. It's called ZStack , and it works identically to the other two stack types.
It's used to layer components on top of each other.
```

 
