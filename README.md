# ASU_iOS12Workshop

Here's the code for the lecture.
Full project will be uploaded soon.

Make a project 

```swift
  

class Ogla{
    private var hair : String?
    private var eyeColor : String?
    private var height : Int?

    init() {
        print("A new ogla is created!")
        hair = "No Hair"
        eyeColor = "Black-White eyes"
        height = 0
    }
    
    init(hair : String?, eyeColor: String?, height: Int?) {
        
        self.hair = hair
        self.eyeColor = eyeColor
        self.height = height
        
    }
    
    
    /*
     Author: Ali Mohammad
     2018
     function to display
     ogla is eating
     */
    func eat(){
            print("Ogla is eating")
    }
    
    func read(){
        print("Ogla is readuing")
    }
    
    func play(){
        print("Ogla is playing GW2")
    }
    
    func program (language : String ){
        print("Ogla will learn how to program with \(language) !)")
    }
    
    func getHair () -> String? {
        return self.hair
    }
    
    func setHair( hair : String? ){
        if hair == nil {
            self.hair = "Bald"
        } else {
            self.hair = hair
        }
    }
    
    func setHair( hair : String?, height : Int? ){
        
        self.height = height
        
        if hair == nil {
            self.hair = "Bald"
        } else {
            self.hair = hair
        }
    }
}


class SmallOgla : Ogla{
    
    override func eat(){
        print("Small ogla is eating badly")
    }
    
}

class GirlOgla : Ogla{
    
    override func play(){
        print("Girl is playing with her dolls")
    }
    
    
    
}

var ogla = Ogla()
ogla.eat()
ogla.setHair(hair:nil,height : 12)
print(ogla.getHair()!)
ogla.program(language: "Swift 4")
var small = SmallOgla()
small.eat()
var girl = GirlOgla()
girl.play()

var ogla1 : Ogla = GirlOgla()
var ogla2 : Ogla = SmallOgla()


    Create a class Person that can be either user or admin.
 In Person:
 private attr:
    id
    name
    age
 public functions:
    get + set Name
    signIn
    signOut
    post
    follow
 In User (functions):
    override follow
    overload post
 In Admin (functions):
    edit Users

protocol Image {
    func setImage (path : String?)
    func getImage () -> String?
    func setSize (width: Int?, height : Int?)
    func calculatePixles () -> Int?
    func onClick() -> Bool?
    func displayImage()
}

class CircleImage : Image {
    
    private var path : String?
    private var width : Int?
    private var height : Int?
    private var radius : Double?
    
    func setImage(path: String?) {
        self.path = path
    }
    
    func getImage() -> String? {
        return self.path
    }
    
    func setSize(width: Int?, height: Int?) {
        self.width = width
        self.height = height
    }
    
    func calculatePixles() -> Int? {
        return ( self.width! * self.height! )
    }
    
    func onClick() -> Bool? {
        print("Got Clicked!")
        return true
    }
    
    func displayImage() {
        
    print("Displaying Circle : \(self.path!) Image With: \(self.radius!) \n Width: \(self.width!) - Height: \(self.height!)" )
    }
    
    init(path : String?, width: Int? , height: Int?, radius: Double? ) {
        self.path = path
        self.width = width
        self.height = height
        self.radius = radius
    }
}

let circleImage = CircleImage(path: "C:/Images/1.png", width: 200, height: 200, radius: 50.0)

circleImage.displayImage()
circleImage.setImage(path: "D:/car.jpg")
circleImage.displayImage()


```
