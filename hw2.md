<h2>HW2</h2>
    
```swift

import SwiftUI

struct ContentView: View{
    @State var count: Int = 0
    @State var playerInt: Int=0
    @State var win: Int = 0
    var emoji: String {
        if count == 1 {
            return "✂️" 
        } else if count == 2 {
            return "🪨" 
        } else if count == 3 {
            return "🧻" 
        } else {
            return ""
        }
    }

    var playemoji: String {
        if playerInt == 1 {
            return "✂️" 
        } else if playerInt == 2 {
            return "🪨" 
        } else if playerInt == 3 {
            return "🧻" 
        } else {
            return ""
        }
    }

    var result: String {
        if win == 0{
            return ""
        }
        else if win == 1{
            return "WIN"
        }
        else if win == 2{
            return "LOSE"
        }
        else if win == 3{
            return "TIE"
        }
        else{
            return ""
        }
    }
    var body: some View{
        HStackLayout{    
            VStack{
                Text(emoji)
                    .padding(.all,10)
                    .frame(width:150 ,height:120 ,alignment: .center)
                    .font(.system(size:100))
            }
            VStack{
                Text(playemoji)
                    .padding(.all,10)
                    .frame(width:150 ,height:120 ,alignment: .center)
                    .font(.system(size:100))
            }
        }
        VStack{
            Text(result)
                .padding(.all,10)
                .frame(width:200 ,height:120 ,alignment: .center)
                .font(.system(size:65))
        }
        Button(action:{
            self.count=Int.random(in: 1...3)
            if(count != 0 && playerInt != 0){
                if(count == playerInt){
                    win = 3
                }   
                else if(count == 1 && playerInt == 2){
                    win = 1
                }
                else if(count == 1 && playerInt == 3){
                    win = 2
                }
                else if(count == 2 && playerInt == 1){
                    win = 2
                }
                else if(count == 2 && playerInt == 3){
                    win = 1
                }
                else if(count == 3 && playerInt == 1){
                    win = 1
                }
                else if(count == 3 && playerInt == 2){
                    win = 2
                }
            }
            else{
                win = 0
            }
        }
               ,label:{
            Text("出拳")
                .padding(.all,10)
                .frame(width: 200, height: 80,alignment: .center)
                .font(.system(size:60))
                .background(Color.purple)
                .foregroundColor(.white)
                .border(Color.purple,width: 5)
                .cornerRadius(20)
        })
        HStack{
            Button(action: {
                self.playerInt=1}
                   , label: {
                Text("✂️")
                    .padding(.all,10)
                    .frame(width: 100, height: 80,alignment: .center)
                    .font(.system(size:60))
                    .background(Color.white)
                    .foregroundColor(.white)
                    .border(Color.white,width: 5)
                    .cornerRadius(20)
            })
            Button(action: {
                self.playerInt=2}
                   , label: {
                Text("🪨")
                    .padding(.all,10)
                    .frame(width: 100, height: 80,alignment: .center)
                    .font(.system(size:60))
                    .background(Color.white)
                    .foregroundColor(.white)
                    .border(Color.white,width: 5)
                    .cornerRadius(20)
            })
            Button(action: {
                self.playerInt=3}
                   , label: {
                Text("🧻")
                    .padding(.all,10)
                    .frame(width: 100, height: 80,alignment: .center)
                    .font(.system(size:60))
                    .background(Color.white)
                    .foregroundColor(.white)
                    .border(Color.white,width: 5)
                    .cornerRadius(20)
            })
        }
    }
}



<img width="40%"  src="https://github.com/Xiang-92/yzu-swiftui-1101421/blob/main/IMG_0309.jpeg">
