<h1>HW1</h1>
    
```swift

      import SwiftUI

struct ContentView: View{
    var body: some View{
        Image("Picture2")
            .resizable()
            .scaledToFit()
            .overlay(
                Text ("1101421    陳昱翔")
                    .fontWeight(.heavy)
                    .lineSpacing(20)
                    .font(.system(size:25))
                    .foregroundColor(.white)
                    .frame(width: 250, height: 100)
                    .background(.blue)
                    .cornerRadius(30)
                    .opacity(0.8)
                ,alignment: .bottom
                )
            .overlay(
            Image(systemName: "heart.fill")
            .font(.system(size: 100))
            .foregroundColor(.pink).opacity(0.6).frame(width:160,height: 160)
            ,alignment: .bottomTrailing
            )
            .overlay(
                Text("努力畢業")
                    .fontWeight(.heavy)
                    .lineSpacing(20)
                    .font(.system(size:25))
                    .foregroundColor(.white)
                    .frame(width: 250, height: 100)
                    .cornerRadius(30)
                    .opacity(0.8)
                ,alignment: .centerFirstTextBaseline
            )

    }
}
struct ContentView_Preview:PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}



    
```

<img width="40%"  src="https://github.com/Xiang-92/yzu-swiftui-1101421/blob/main/IMG_0309.jpeg">
