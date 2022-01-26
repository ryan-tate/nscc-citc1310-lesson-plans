Welcome back!  This week we're going to begin 

If you were NOT here last week, please raise your hand, I just need to know who you are for roll purposes.

We're going to go ahead and jump right into Chapter 2: Getting Started with Forms and Controls

# Chapter 2

> The first step in creating a Visual C# application is creating the application's GUI.  

Let's go ahead and open Visual Studio 

We'll create a new Project and remember we'll be using __Windows Forms App (.NET Framework__ for our project type.

Let's name our Project Chapter 2 Demo

### The Application's Form

As you can see, when we created our new project, a new form was created automatically for us. As we saw last week, it's just an empty form with no controls and it is displayed in Designer view.

This is where we will begin designing the interface for our application. From here we can add controls, change the properties and characteristics like size and color.

Our form is currently selected, and we get what is known as a __BOUNDING BOX__ around it showing that it is our currently selected item and we'll see sizing handles displayed for quickly editing the object's size

### Identifying Forms and Controls by Name

An application's GUI is made of forms and controls. Each form and control in a GUI must have a name that identifies it. The blank form we get by default has a name of __Form1__

For now, we can leave this as Form1, though later on we'll see why we would change this.

### Properties Window

You may remember that last week we discussed the properites window. The appearance and other characteristics about each object are determined by that object's properties. When you select an object in designer, the object's properties are displayed in the Properties window.

You may also recall from last week that the NAME of the object that is currently selected is shown at the top of the properties window.

When we look at the properties list, on the left we see the NAME of each property and on the right we see the value for that property.  For example, our form has a property named Locked and the Locked property has a value of FALSE

Let's go ahead and change the Text on our form.

To do that, let's find the Text property, then change the value of that property.

_Change Text to My First Prograom_

Let's try changing the object's size property as well.

### Add Controls to a Form

You may also recall from our quick tour of Visual Studios that we have sommething called the Toolbox, which is where we find controls that can be added to our form.

Let's begin adding some controls now.

To add a control from the toolbox, recall that you can double-click it or drag from the toolbox and drop onto your form canvas

Let's add a button to our form 

_Add Button_

### Resizing and Moving Controls 

Notice that our button is selected, it is enclosed by a bounding box and has resize handles shown around that box. With the object selected, we can drag the control to another location in our form, and we can also resize the control using the sizing handles.

### More About Buttons

When we work with buttons, one property we should ALWAYS change is the text. The text on a button should clearly identify the button's purpose. You would expect to normally see things like _Calculate Average_ or _Print Report_ on a button so that a user knows what should happen when the button is clicked.

Keep in mind that while the button's text and its name intially have the same value, they are separate properties. The Text should hold a friendly, readable value for the user, while the name identified how the control will be referenced in code.

### Changing a Control's Name

In addition to changing the text, button names should be changed to something more meaningful as well.  Imagine the toolbar on something like Microsoft word, think of how many button controls. If you're working in code, what is more meaningful, something like btnSaveAs or button214.

In this course, you should always identify the type of control, then (using camel case) identify the control's purpose or function.  A button that calculates taxes for instance may have a text property of 'Calculate Tax' and a name of 'btnCalculateTax'

The __NAME__ cannot contain spaces, but the text can.

> #### NOTE: The book does not specifically teach the method I have discussed for prefacing the control's name with the control type, but you WILL BE EXPECTED TO FOLLOW THIS IN YOUR ASSIGNMENTS.  This is known as Hungarian Notation



## 2.2 Creating the GUI for your first Visual C# Application

We worked throught this example, or one very similar to it last week, but let's take the time to do it again to get familiar with the process of building a simple GUI.

We're going to divide this this two big parts: First we are going to design and build the application interface and second we'll write the code that causes the Hello World message to appear when the user clicks the Display message button.

Add Button, Set Text, Set Name

Start App to show it runs but does nothing

## 2.3 Introduction to C# Code 

Let's go ahead and open our code by right-clicking Form1.cs in the Solution Explorer and choosing View Code.

Recall that last week we briefly discussed that the 'using' statements you see at the top of this are references to other __namespaces__.  A Namespace is a container that holds classes, classes are containers that hold methods, and methods are a grouping of one or more programming statements that perform some operation.

So the 'using' directives here load other namespaces into our code file, and we're creating our OWN namespace here as well.

We create a new namespace named Chapter_2_Demo and we enclose the entire namespace in a set of curly braces 

Inside our Chapter_2_Demo namesapce we have a new Class called Form1.  Like our namespace, the class is also warpped in curly braces.

> Pay attention to code formatting and indentation.  VS does a good job of doing this for you but I will expect the code you turn in to be readable! Don't give me a file with no identation and expect full credit!  If I cannot read your code, even if it compiles and runs correctly, I will deduct points.

Finally, the `public Form1()` part is a method and `InitializeComponent()` is currently the only statement in that method

### Adding Code

What we're going to do now is code a special type of method know as an __event handler__ because it __handles__ or responds to a specific __event__ or action in your application.  Specifically here, we want to handle (or respond) to the click event of our button.  

To get started, in my Designer, I'm goign to DOUBLE CLICK the button. WHen I do that, we'll see a new method called `btnDisplayMsg_Click` is created in our code automagically.

This event handler exists and would technically fire if we clicked our button, but it doesn't contain any code so at the moment, it still wouldn't DO anything if we clicked the button.

We need some code!

For now, we want to display a Message Box or dialog box when the button is clicked.  So let's add this code `MessageBox.Show("Hello, World!");`

#### String Literals

We haven't really discussed data types yet, but as with any programming language, C# has certain data types.  One of these is a string, which is basically just text. In our example, we passed a string "Hello, World!" to the MessageBox.Show() method.  When a piece of data is written into the program's code, it's called a "literal" becasue the data is literally written into the program.  This is also sometimes called "hard coding."  So "Hello, World" is a __string literal__.

In C#, __string literals__ must be enclosed in DOUBLE quotation marks.

#### Multiple Buttons with Multiple Event Handlers 

Let's add a few more buttons `btnSecond` and `btnThird`  and let's attach event handlers to each.  We'll use a simple message box again to show some distinct message on each


### Design Time and Run Time

We'll talk throughout the development process about things that can occur at design time and run time.  When you have a project open in VS and you're building a GUI or writing the application's code, that's referred to as __design time__.  During design time, you can use the Designer and the Toolbox to place controls, use the Properties window to set property values, use the code editor to write code, and so on.

When you actually are ready to execute the program and press <kbd>F5</kbd> or click the Start button on the toolbar, the program will be compiled. If there are no compiler errors, the program is executed. The time during which an app is running is called run time. During that time you can interact with the interface, but you cannot access Designer or change the application's code.

## 2.5 Label Controls

So we've worked with some buttons, but we'll need more than just button controls in most applications. Another very common control type is a label. 


As you might exepct, this label can be changed at design time, and can PROGRAMMATICALLY be changed at run time, but a user cannot directly interact with a label control like that can a textbox, for example.  

Let's clean up our application and start with just a label.  When we add the label, it gets a generic name and text property like 'label1'.  I'm going to change my label's text property to say "This is a label control".  Normally, we'd want to give this a more meaningful name, too.

Let's look at some of the other properties we can set on our label.

Let's find the __Font__ property and expand it. We see seveal child properties here, font name, size, etc.  Let's modify a few of these and see our label change.

Next, find the BorderStyle property.  Check out the different border styles available.

Notice that our label, unlike the button, does NOT have sizing handles around it.  By default, labels are set to auto size.  You can toggle this by setting the label's __AutoSize__ proeprty to false.  If we do that, we can manually choose the size of our label control.

Next, let's find the __TextAlign__ property.  Adjust this property to change where your text is anchored (aligned) within the control.

### Using Code to Display Output in a Label Control

So far, we've been setting the label's value at Design Time.  Another use of a label is to show output at run time.

Let's add a button back to our APplication and call it btnDisplayMsg again. I'll set the text of the button to "Click Me" 

Below that, let's add a label. 
* name: lblOutput
* text: (none)
* AutoSize: false
* size: (large enough)

Now let's add an event handler to our button by double-clicking the BUTTON

```C#
private void btnDisplayMsg_Click(object sender, EventArgs e)
{
  lblOutput.Text = "Thank you for clicking the button";
}
```
