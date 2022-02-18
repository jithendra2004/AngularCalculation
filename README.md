# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```HTML
app.component.html:
<style>
    *{
box-sizing: border-box;
font-family: Arial, Helvetica, sans-serif;
}

body{
background-color: rgb(226, 164, 207);
color: black;
}

.container{
text-align: center;
width: 1080px;
height: 730px;
margin-left: auto;
margin-right: auto;
margin-top: auto;
}

.content{
display: block;
width: 100%;
margin-left: auto;
margin-right: auto;
background-color: rgb(233, 202, 145);
margin-top: 25px;
min-height: 275px;
}

.content1{
display: block;
width: 100%;
margin-left: auto;
margin-right: auto;
background-color: rgb(233, 202, 145);
margin-top: 25px;
min-height: 300px;
}

h1{
color: rgb(0, 0, 0);
text-align: center;
padding-top: 20px;
}

h2{
color: rgb(0, 0, 0);
text-align: center;
padding-top: 20px;
}

.formelement{
text-align: center;
padding-top: 20px;
font-size: larger;
}


.footer{
display: inline-block;
width: 100%;
height: 35px;
background-color: darksalmon;
color: black;
text-align: center;
padding-top: 7px;
font-size: large;
}

</style>

<body>
    <div class="container">
    <h1>Math Calculations</h1>
    <div class="content">
        <Cylinder-Area class="formelement"></Cylinder-Area>
    </div>
    <div class="content1">
        <Rectangle-Area class="formelement"></Rectangle-Area>
    </div>
    <div class="footer">
        Developed by Harikrishna 
    </div>
    </div>

</body>
app.module.ts:
import { NgModule } from '@angular/core'; import { FormsModule } from '@angular/forms'; import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component'; import { cylinderComponent } from './cylinder/cylinder.component'; import { RectangleComponent } from './rectangle/rectangle.component';

@NgModule({ declarations: [ AppComponent,RectangleComponent,cylinderComponent ], imports: [ BrowserModule,FormsModule ], providers: [], bootstrap: [AppComponent] }) export class AppModule { }
##cylinder.component.html:

<div>
    <h2>Area of a Cylinder</h2>
    Radius=<input type="text" [(ngModel)]="radius"> Meters<br/>
    height=<input type="text" [(ngModel)]="height"> Meters<br/>
       <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Area=<input type="text" [value]="area"> Meters<sup>2</sup><br/>
</div>
cylinder.component.ts:
import { Component } from "@angular/core";

@Component({
    selector:'Cylinder-Area',
    templateUrl:'./cylinder.component.html'
})
export class cylinderComponent{
    radius:number;
    height:number;
    area:number;
    constructor(){
        this.radius=10;
        this.height=20;
        this.area= this.radius * this.height;
    }
    onCalculate(){
        this.area =(22/7)* this.radius*this.radius * this.height
    }
}
rectangle.component.html:
<div>
    <h2>Area of a Rectangle</h2>
    Length=<input type="text" [(ngModel)]="length"> Meters<br/>
    Breadth=<input type="text" [(ngModel)]="breadth"> Meters<br/>
       <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Area=<input type="text" [value]="area"> Meters<sup>2</sup><br/>
</div>
rectangle.component.ts:
import { Component } from "@angular/core";

@Component({
    selector:'Rectangle-Area',
    templateUrl:'./rectangle.component.html'
})
export class RectangleComponent{
    length:number;
    breadth:number;
    area:number;
    constructor(){
        this.length=10;
        this.breadth=20;
        this.area= this.length * this.breadth;
    }
    onCalculate(){
        this.area = this.length * this.breadth
    }
}
```
## OUTPUT:

### Home Page:


## Result:
