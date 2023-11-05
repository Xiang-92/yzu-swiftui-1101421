<h3>HW3</h3>
    
```swift

import SwiftUI
struct ContentView: View{
    var body: some View{
        VStack{
            TitleView()
            HStack{
                DollarView(imageName: "100",imageTitle: "一百塊")
                DollarView(imageName: "200",imageTitle: "兩百塊")
            }
            ZStack{
                ThousandView()
                Text("這個我沒有那麼多")
                    .font(.system(size: 20))
                    .foregroundColor(.yellow)
                    .padding(.all, 5)
                    .background(Color.black)
                    .opacity(0.7)
            }
            FhundredView()
        }
    } 
}

struct TitleView: View{
    var body: some View{
        VStack(alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/, spacing: 2) {
            Text("Chris的")
                .font(.system(size:30))
            Text("保險箱")
                .font(.title)
                .foregroundColor(Color(red: 29 / 255, green: 40 / 255, blue: 192 / 255))
        }
    }
}

/*struct HundredView: View{
    var body: some View{
        VStack{
            Image("100")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 180 ,alignment: .center)
            Text("一百塊")
                .fontWeight(.bold)
                .font(.system(size: 30))
        }
    }
}*/

/*struct ThundredView: View{
    var body: some View{
        VStack{
            Image("200")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 180 ,alignment: .center)
            Text("兩百塊")
                .fontWeight(.bold)
                .font(.system(size: 30))
        }.padding(.all, 2)
    }
}*/

struct ThousandView: View{
    var body: some View{
        VStack{
            Image("1000")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .padding(.all, 15)
            Text("一千塊")
                .fontWeight(.bold)
                .font(.system(size: 30))
        }
    }
}


struct FhundredView: View{
    var body: some View{
        VStack{
            Image("500")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .padding(.all, 15)
            Text("五百塊")
                .fontWeight(.bold)
                .font(.system(size: 30))
        }
    }
}

struct DollarView: View{
    var imageName:String
    var imageTitle:String
    var body:some View{
        VStack{
            Image(imageName)
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(height: 120, alignment: .center)
            Text(imageTitle.capitalized)
                .fontWeight(.bold)
                .font(.system(size: 25))
        }
        .frame(minWidth: 0, idealWidth: 100, maxWidth: .infinity, minHeight: 0, idealHeight: 100, maxHeight: .infinity, alignment: .center)
    }
}

extension UIScreen{
    static let screenWidth = UIScreen.main.bounds.size.width
    static let screenHeight = UIScreen.main.bounds.size.height
    static let screenSize = UIScreen.main.bounds.size
}

```


<img width="40%"  src="https://github.com/Xiang-92/yzu-swiftui-1101421/blob/main/IMG_0311.jpeg>
