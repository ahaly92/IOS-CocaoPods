# IOS - CocoaPods

## What is CocaoPods?

CocoaPods is a dependency manager like Gradle in Android or NPM in the Web world

## Setting up CocaoPods
1. Open XCode & create a new project: CMD+SHIFT+N
2. Close the project & open the terminal 
3. Install CocoaPods run: sudo gem install cocoapods [this is a global command so you can run it from anywhere]
4.  Move to the project directory, you can do this with cd path/to/project/
5.  Initialize a CocoaPods project by typing pod init in your iOS project’s root directory.
6.  Open the newly generated Podfile in an IDE or text editor.
7.  Search for available pods on the website: https://cocoapods.org/
8.  Inside the Podfile, after the line # Pods for [project-name] add your pod by typing pod 'RxSwift' or whatever your pod is named.
9.  Now make sure the XCode project is closed, then in the terminal (while still in the project root directory) run the command pod install this will download all the CocoaPods into a folder called Pods/ and generate a .xcworkspace (white) project.
10.  Open the .xcworkspace with XCode, now anywhere in your swift code you can use the library by importing it at the top of the file. ex: import RxSwift

You won’t need to install CocoaPods every time.

## Pro (?) Tips!
1. Add new pods by typing them in the Podfile and typing pod install in the root directory again.
2. To determine if Cocoapods is installed, run gem which cocoapods anywhere in the terminal. If nothing is returned then Cocoapods isn’t installed. If it is installed then you should see something like this: /Library/Ruby/Gems/2.3.0/gems/cocoapods-1.5.3/lib/cocoapods.rb
3. If the project doesn’t build, try cleaning it with CMD+SHIFT+K
4. If your project still doesn’t build, navigate to the derived data folder and delete it. Rebuilding the project will generate a new derived data folder.
5. The Podfile.lock is used for generating the exact copy of modules you used. This is useful if you don’t commit your pods in a git repo and someone clones your project.
6. The CocoaPods team recommends that you commit your Pods/
7. You should never directly edit anything in the Pods/ directory. If you were to install a new pod then your changes would be reverted.
8. Alternatively you could use Carthage, but it seems that CocoaPods have become the more popular choice: https://github.com/Carthage/Carthage
