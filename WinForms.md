## Developing WinForms in O2 ##

So I'm assuming you have followed the Web Automation guide and you're getting more ambitious with your scripting.
You may be at the point now then where you want to interact with the user before, or during the time that the script is running.
An example of this is my Google hacking tool. Note this that this tool does not "hack" Google, it uses the operators Google offers to refine your searches and ultimately return much more relevant results. When I first created it, the user had to hard code into the script the Google search they wanted to run. OK for one off hacks, but not great if you want to use the tool more and more for different purposes. I also have an appalling memory when it comes to things I know are available on Google. I needed some drop down boxes.....

Some of this stuff was touched on in the web automation guide, but only to aid in the examples. I may take it out of there when these guides start to come together. Here I'll try and go into more detail.

<a name="contents"></a>
#Contents#

- [The UI Area](#uiArea) 
- [Labels](#labels)
- [Text Boxes](#textBoxes)
- [Buttons](#buttons)
- [CheckBoxes](#checkBoxes)
- [DropDown Boxes](#dropdowns)
- [Mix and match!!](#mixmatch)
- [Alert Boxes](#alerts)
- [Ask The User](#requests)
- [DataGrid Views](#datagrids)
- [Examples](#examples)
- [Appendix](#appendix)

<a name="uiArea"></a>
##The UI Area
[Go to Contents](#contents)

When beginning a new script the first thing you need to do is bring inject an instance of a web browser into O2. 
To do this we create a panel within O2, then insert an instance of Internet Explorer into that:

    var topPanel = panel.clear().add_Panel();
	var ie = topPanel.add_IE();

<a name="labels"></a>
##Labels
[Go to Contents](#contents)

Labels are what they say on the tin. They can't be edited by the user but they can give a user an idea of what they are supposed to do:

	actionPanel.add_Label("I am a label...");

Absolute location of any element can be set with the top(), left(), right(), bottom() methods:

	actionPanel.add_Label("OP1:").top(20).left(100);

Will set the label 20 pixels from the top and 100 from the left. It can be quite fiddly laying out UI's so as time goes on its worth building seperate scripts for them and calling them, or building C# classes to handle it. Also setting locations to variables that can be called on is a neater way of dealing with the layout issue.

<a name="textBoxes"></a>
##Text Boxes
[Go to Contents](#contents)

<a name="buttons"></a>
##Buttons
[Go to Contents](#contents)

<a name="checkBoxes"></a>
##CheckBoxes
[Go to Contents](#contents)

Checkboxes are pretty straight forward to use. This snippet will pop an alert up each time the checkbox changes state. Its slightly confusing because onChecked() sounds like when its set to true, but its whenever it changes state....

	actionPanel.add_CheckBox(0, 0,"!").onChecked((value)=> {
																	value.str().alert();
                                                           });
You can set a global to the value to use it elsewhere....

<a name="dropdowns"></a>
##DropDown Boxes
[Go to Contents](#contents)

<a name="#mixmatch"></a>
##Mix And Match!!
[Go to Contents](#contents)

<a name="alerts"></a>
##Alert Boxes
[Go to Contents](#contents)

<a name="requests"></a>
##Ask The User
[Go to Contents](#contents)

<a name="datagrids"></a>
##DataGrid Views
[Go to Contents](#contents)

<a name="examples"></a>
##Examples
[Go to Contents](#contents)

<a name="apppendix"></a>
##Appendix
[Go to Contents](#contents)