# TestDom_Multiple_choices
## TestDom Q&amp;A multiple choices
## Question 1 Component (Angular)

Which of the following statements about components in Angular are correct?

(Select all acceptable answers.)

```sh
When a component depends on a service, the injector can be used to configure dependency injection. (correct)
A component defines its input parameters with the @Input decorator. (correct)
A components ngOnDestroy method is called just before Angular destroys the component. (correct)```


## Question 2 Color Type (Typescript)


The following code initializes three types representing the colors: red, green and blue.
```sh

type ColorType = [string, number, number, number];
let red: ColorType = ['Red', 1, 0, 0];
let green: [string, number, number, number] = ['Green', 0, 1, 0];
let blue = ['Blue', 0, 0, 1];
```

Select the statements that are correct.

```sh
(Select all acceptable answers.)
ColorType is an alias to a tuple.  (correct)
All three colors would compile to the same JavaScript type signature. (correct)
ColorType is an array where the type of a fixed number of elements is known. (correct)
```

## Question 3 Welcome

Consider the following component:
```sh

import { Component, Input } from '@angular/core';

@Component({
  selector: 'welcome',
  template: `<h1>Welcome to {{name}}!</h1>`,
  styles: [`h1 { font-family: Lato; }`]
})
export class WelcomeComponent  {
  @Input() name: string;
}
Select the statements about its use (in another components template or module) that are correct.
```


```sh
(Select all acceptable answers.)

<welcome name="TestDome"></welcome> will display: "Welcome to TestDome!".  (correct)
@NgModule({ declarations: [ WelcomeComponent ] }) export class WelcomeModule {} declares that the welcome component belongs to the welcome module. (correct)

```

## Question 4 Animal Noise

Consider the following component, which can be used to model an animal and the noise it makes.

```sh
import {Component, Input, Output} from '@angular/core';

@Component({
  selector: 'animal-noise',
  template: `
    <span>{{animal}}</span>
    <button (click)="makeNoise()">Make noise</button>
  `
})
export class AnimalNoise {
  @Input('animal') animal: string;
  @Input('noise') noise: string;

  makeNoise() {
    alert(`${this.noise}`);
  }
}

```

Select the statements about the AnimalNoise component that are correct.

```sh
(Select all acceptable answers.)
The 'animal' parameter of the @Input('animal') declaration does not alter the interface of the component. (correct)

When included in a components template, the AnimalNoise component creates a span containing the interpolated animals name and a button bound to makeNoise().   (correct)

```

## Question 5 Cache Casting

A company is designing the class hierarchy for various cache implementations:
```sh
public class Cache {}

public class DiskCache extends Cache {}

public class MemoryCache extends Cache {}

public class OptimizedDiskCache extends DiskCache {}


```
Select all the answers that will result in a runtime exception.
(Select all acceptable answers.)

```sh
MemoryCache memoryCache = new MemoryCache();
Cache cache = (Cache) memoryCache;
DiskCache diskCache = (DiskCache) cache;   (correct)


DiskCache diskCache = new DiskCache();
OptimizedDiskCache optimizedDiskCache = (OptimizedDiskCache) diskCache; (correct)

Cache cache = new Cache();
MemoryCache memoryCache = (MemoryCache) cache; (correct) 

```


## Question 6 UITableView (Ios/Swift)

Select the components that are minimally required for constructing and configuring a UITableViewController, which can be used to view (but not manipulate) a list of items.

(Select all acceptable answers.)

```sh
UITableViewCell.  (Correct)
UITableViewDataSource.  (Correct)

```

## Question 7 View Controller (Ios/Swift)

Which of the following statements are true for UIViewController?

(Select all acceptable answers.)

```sh
viewWillAppear will be called before a view appears on the screen. (Correct)
When using storyboards, the controller is initialized with the init(coder:)/initWithCoder method.  (Correct)
View controllers manage a hierarchy of views. (Correct)

```
## Question 8 Events (Ios/Swift)
Which of the following statements are true for user interface events in iOS?

(Select all acceptable answers.)
```sh
Touch up inside is an event provided by UIControl. (Correct)
Touch events can be cancelled.  (Correct)
The first responder to an event can be changed. (Correct)
Capturing swipe events is supported through a gesture recognizer. (Correct)

```

## Question 9 Car (Ios/Swift)
Consider the following Swift definition of the structure Car:
```sh
struct Car {
    var color:UIColor?
    let model:String
    
    init(model:String) {
        self.model = model
        self.color = nil
    }

    mutating func changeColor(color:UIColor) {
        self.color = color
    }
}

```
Select the statements that are correct.

(Select all acceptable answers.)
 ```sh
The property model cannot be changed after initialization. (Correct)
The mutating keyword of changeColor is required to modify the instance variable color.  (Correct)

```

## Question 10 Even Numbers (javascripts)

A Mathematics tutoring web application for kids has a button that highlights all even numbers (in span), using 'yellow' as the background color. Clicking the button again removes the background. All further clicks add or remove the 'yellow' background alternately.

Currently, the button doesn't work as expected. For the given HTML markup and JavaScript function, select all options that will identify and fix the bugs in the JavaScript function:

```sh
<div id='numbers'>
 <span>1</span><span>2</span><span>3</span><span>4</span><span>5</span>
 <button id='btn' onclick='toggleEvenColor()'>Toggle even number highlighting</button>
</div>
```

```sh
1: function toggleEvenColor() {
2:   let spanElements = document.querySelectorAll('#numbers span');
3:   spanElements.forEach(function() {
4:     item.style.backgroundColor = 'transparent';
5:   });
6: }

```
(Select all acceptable answers.)

```sh
At line number 2, use let spanElements = document.querySelectorAll('#numbers span:nth-child(2n)'); (Correct)
At line number 3, define item as a parameter for the anonymous function passed in forEach. (Correct)
At line number 4, use item.style.backgroundColor = item.style.backgroundColor !== 'yellow' ? 'yellow' : 'transparent'; (Correct)

```

## Question 11 Positionable (TypeScript)
Consider the following code:
```sh
class Positionable {
  locationX: number = 0;
  locationY: number = 0;
  moveTo(toX: number, toY: number) {
    this.locationX = toX;
    this.locationY = toY;
  }
}

class Rotatable {
  orientation: number = 0;
  rotate(orientation: number) {
    this.orientation += orientation;
  }
}

class MovingObject {
  locationX: number = 0;
  locationY: number = 0;
  orientation: number = 0;
  printPosition(){
    console.log(this.locationX, this.locationY);
  }
}

function applyMixins(derivedCtor: any, baseCtors: any[]) {
  baseCtors.forEach(baseCtor => {
    Object.getOwnPropertyNames(baseCtor.prototype).forEach(name => {
      derivedCtor.prototype[name] = baseCtor.prototype[name];
    });
  });
}

applyMixins(MovingObject, [Positionable, Rotatable]);
let mover = new MovingObject();

```
Select the statements that are correct.

(Select all acceptable answers.)
```sh
After the last line of code, rotate and moveTo can be called on mover. (Correct)
The printPosition method still exists on MovingObject after applyMixins is called. (Correct)
```


Thanks to [Github](https://github.com/0788611515), [TestDome](https://www.testdome.com),  and [Stack Overflow](https://stackoverflow.com/users/14854653/sensei-alex-sylvain-luenga)

