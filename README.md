# CHIPageControl For SALPay

CHIPageControl/aji is an updated aji animated page control to replace boring UIPageControl.

forked with ChilliLabs [CHIPageControl](https://github.com/ChiliLabs/CHIPageControl.git)
Made with ❤️ by [Chili](http://chi.lv).

Forked/Updated by Jorel Cruz

## Overview

<img src="Images/Aji.gif" width="600" height="450">

## Requirements
* Swift 4.2

## Installation

### Manually

Just add the `CHIPageControl` folder to your project.

### CocoaPods

use [CocoaPods](https://cocoapods.org) with Podfile:
```
# individual page control
pod 'CHIPageControl/Aji'  :git => 'https://github.com/jorelkimcruz/CHIPageControl.git'
```

## Usage
### 🎨 Storyboards
Just drop UIView and set its class to be one of CHIPageControls.
<img src="Images/ibdesignable.gif" width="800" height="564">
### 💻 Code
``` swift
let pageControl = CHIPageControlAji(frame: CGRect(x: 0, y:0, width: 100, height: 20))
pageControl.numberOfPages = 4
pageControl.radius = 4
pageControl.tintColor = .red
pageControl.currentPageTintColor = .green
pageControl.padding = 6
```

### Adding multiple tintColors
``` swift
// The size of the array needs to match the numberOfPages or it will throw an fatal error
pageControl.tintColors = [UIColor.black, UIColor.yellow, UIColor.black, UIColor.black]

// or

// If it is the first one, it will fill all colors with the selected tintColor and then replace the colors with the desired one
pageControl.insertTintColor(UIColor.yellow, position: 1)
```

### Updating progress
``` swift
//update dynamically
pageControl.progress = 0.5

//set progress with animation
pageControl.set(progress: 2, animated: true)
```
### Page Controls 🌶️🌶️🌶️

<img src="Images/Aji.gif" width="100" height="50"> CHIPageControlAji

### PageControlDelegate
``` swift 

//set delegate
pagecontrol.delegate = self

// Returns clicked control
func didClickIndex(_ index:Int) {
    
}
```

## License
CHIPageControl is released under the MIT license. See [LICENSE](./LICENSE) for details.
