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

## New View

```
Right Click the View Group And Select New File. Select SwiftUIView and click on the next button. 
```

## Show/Hide Preview

```
option + command + enter
```

## Global Search

```
cmd + shift + h 
```

## ZStack

```
SwiftUI has a dedicated stack type for creating overlapping content, which is useful if you want to place some text over a picture for example. It's called ZStack , and it works identically to the other two stack types.
It's used to layer components on top of each other.
```

```
Select the button and using thrid option from the right , select it and modify appearance to dark.
```

## TabView 

```
import SwiftUI
struct OnboardingView: View {
    var body: some View {
        TabView {
            ForEach(0..<5){
                item in FruitCardView()
            }
        }
        .tabViewStyle(PageTabViewStyle())
        .padding(.vertical,20)
    }
}
struct OnboardingView_Previews: PreviewProvider {
    static var previews: some View {
        OnboardingView()
    }
}
```
 
 ## Components & Methods
 
 ```
 ForEach
 @State
 @main
 @AppStorage
 @Environment
 ZStack
 VStack
 HStack
 Image
 View
 Text
 TabView
 PreviewProvider
 LinearGradient
 Divider
 Spacer
 DisclosureGroup
 GroupBox
 Group
 Link
 Button
 NavigationView
 List
 ScrollView 
 Toggle
 NavigationLink
 ```
 
 ## Properties
 
 ```
 ContentView(fruits: fruitsData)
 .previewDevice("iPhone 11 Pro")
 .previewLayout(.fixed(width: 375, height: 60))
 .preferredColorScheme(.dark)
 .previewLayout(.sizeThatFits)
 .padding(.horizontal, 16)
 .padding(.vertical, 10)
 HStack(spacing: 8)
 Image(systemName: "arrow.right.circle")
          .imageScale(.large)
 .onAppear() {
     withAnimation(.easeOut(duration: 0.5)) {
      isAnimatingImage = true
    }
  }
  .onDisAppear {}
  // SwiftUI gives us equivalents to UIKit’s viewDidAppear() and viewDidDisappear() in the form of onAppear() and onDisappear(). 
 .background(
        Capsule().strokeBorder(Color.white, lineWidth: 1.25)
      )
 .accentColor(Color.white)
 LinearGradient(gradient: Gradient(colors: fruit.gradientColors), startPoint: .topLeading, endPoint: .bottomTrailing)
 Link("Wikipedia", destination: URL(string: "https://wikipedia.com")!)
 Image(fruit.image)
  .resizable()
  .scaledToFit()
  .shadow(color: Color(red: 0, green: 0, blue: 0, opacity: 0.15), radius: 8, x: 6, y: 8)
  .scaleEffect(isAnimating ? 1.0 : 0.6)
   Text("If you wish, you can restart the application by toggle the switch in this box. That way it starts the onboarding process and you will see the welcome screen again.")
   .padding(.vertical, 8)
   .frame(minHeight: 60)
   .layoutPriority(1)
   .font(.footnote)
   .multilineTextAlignment(.leading)
 ```
 
 ## DataModel

```
struct Fruit: Identifiable {
  var id = UUID()
  var title: String
  var headline: String
  var image: String
  var gradientColors: [Color]
  var description: String
  var nutrition: [String] 
}
```

## Apps = n * Scenes = m * Views
 
