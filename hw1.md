<h1>HW1</h1>
    
```swift

      import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack{
            Rectangle()
                .fill(Color(red: 255/255, green: 255/255, blue: 203/255))
                .frame(minWidth: 0, idealWidth: 100, maxWidth: .infinity, minHeight: 0, idealHeight: 100, maxHeight: .infinity, alignment: .center)
                .ignoresSafeArea(.all)
            VStack{
                Text("學號         你的名字")
                    .font(.system(size: 45, weight: .bold))
                    .frame(width: 400, height: 100, alignment: .center)
                    .padding(.top, 0)
                    .offset(x: 0, y: 0)
                Image("ryan")
                    .resizable()
                    .aspectRatio(contentMode: .fill)
                    .frame(width: 600, height: 500, alignment: .trailing)
                    .overlay(
                        Text("112-1\n微型應用程式設計實務\n上課要帶iPad\n在1201A教室上課")
                            .fontWeight(.heavy)
                            .lineSpacing(20)
                            .font(.system(size: 32.0))
                            .foregroundColor(.white)
                            .frame(width: 350, height: 360, alignment: .center)
                            .background(Color.blue)
                            .cornerRadius(25.0)
                            .opacity(0.8)
                            .offset(x: 0, y: 55)
                            .multilineTextAlignment(.center)
                        , alignment: .bottom
                    )
                    .padding(.all, 0)
                    .offset(x: 0, y: -10)
            }
            Image(systemName: "graduationcap.fill")
                .font(.system(size: 60, weight: .bold))
                .offset(x: 0, y: 325)
                .foregroundColor(Color(red: 45/255, green: 63/255, blue: 111/255))
        }
    }
}


    
```

<img width="40%"  src="https://raw.githubusercontent.com/ncudemo/yzu-swiftui-1121-864106/main/hw1-20231002-1.png">
