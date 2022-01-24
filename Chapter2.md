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

> #### NOTE: The book does not specifically teach the method I have discussed for prefacing the control's name with the control type, but you WILL BE EXPECTED TO FOLLOW THIS IN YOUR ASSIGNMENTS.





