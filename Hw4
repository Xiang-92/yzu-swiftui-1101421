<h1>HW4</h1>
    
```swift

      import SwiftUI

struct ContentView: View {
    var body: some View {
        Text("點菜")
            .font(.largeTitle)
            .fontWeight(.heavy)
            .foregroundStyle(.primary)
        TabView{
            Group{
                WelcomeView()
                    .tabItem { 
                        Image(systemName: "rosette")
                        Text("Welcome")
                    }
                CourseListView()
                    .tabItem { 
                        Image(systemName: "list.dash")
                        Text("Courdes")
                    }
                CardView()
                    .tabItem {
                        Image(systemName: "book")
                        Text("Learn")
                    }
            }
            .toolbarBackground(Color.black, for: .tabBar)
            .toolbarBackground(.visible, for: .tabBar)
        }
        .tint(.yellow)
    }
}
struct WelcomeView: View {
    var body: some View{
        VStack{
            Image("關東煮")
                .resizable()
                .aspectRatio(contentMode: .fit)
            Text("呷本\n不好吃就算你兩倍")
                .fontWeight(.heavy)
                .lineSpacing(20)
                .font(.system(size: 32))
                .foregroundColor(.white)
                .frame(width:350,height:150,alignment: .center)
                .background(Color.blue)
                .cornerRadius(20.0)
                .multilineTextAlignment(.center)
        }
    }
}


    
```

<img width="40%"  src="https://github.com/Xiang-92/yzu-swiftui-1101421/blob/main/IMG_0313.jpeg">
