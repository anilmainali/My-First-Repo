![01mlt1md_instockitems](https://cloud.githubusercontent.com/assets/10678180/8501797/a8c20604-216e-11e5-83eb-7e312d7136f1.PNG)

 1.In the TruClient window, click the Toolbox vertical tab to reveal its options.

 2.Select Miscellaneous.

![02mlt1md_evadragjs](https://cloud.githubusercontent.com/assets/10678180/8501799/b0c2415c-216e-11e5-8420-fd92df6be4af.png)


 3.Drag Evaluate JavaScript and drop it above the step.

![03mlt1md_clickoncode](https://cloud.githubusercontent.com/assets/10678180/8501803/b53441a4-216e-11e5-8845-31460b9f8281.PNG)

 4.Click on [Code] to edit.
 
 5.Type in this line to instantiate a variable named content to hold the innerHTML obtained from the screen.

```
var content = document.getElementById('content-inner').innerHTML;
var re = /<td>In Stock<\/td>\s+<td><input name="bookId\[\]" value="([A-z0-9]+)"\stype="checkbox">/g;
match = re.exec(content);while (match != null) {
  TC.setParam("Step3Value_" + counter.toString(),match[1]);
  match = re.exec(content); counter++;
}
TC.setParam("Step3Value_count",counter);
```

Next,

![04mlt1md_forloop](https://cloud.githubusercontent.com/assets/10678180/8501804/ba8b64ca-216e-11e5-8ba8-4c521d752660.PNG)

 1.In the TruClient window, click the Toolbox vertical tab to reveal its options.
 2.Select Flow Control.

![05mlt1md_forloopposi](https://cloud.githubusercontent.com/assets/10678180/8501805/c2a6a82c-216e-11e5-8bae-aa8070da2694.PNG)

 3.Drag For Loop and drop it below the Evaluate JavaScript step you just worked on.

![06mltmd_clickonvari](https://cloud.githubusercontent.com/assets/10678180/8501809/ce86d220-216e-11e5-92eb-5197969266b0.PNG)

 4.Click on var i=0 to edit

![06amltmd_clickeachjs](https://cloud.githubusercontent.com/assets/10678180/8502564/495471b2-2177-11e5-942a-26517fbd125b.PNG)


 5.Click on each JS and change the code as per the above screenshot which is:

```
Init: var i = 1
Condition: i < eval(TC.getParam("Step3Value_count"))
Increment: i++
```

 Next, 

 1.In the TruClient window, click the Toolbox vertical tab to reveal its options.
 
 2.Select Miscellaneous.
 
 3.Drag Evaluate JavaScript and drop it below the For Loop step.
 
 4.Click on [Code] to edit.
 
 5.Type in this line of code.

```
Step3Value=window.Step3Value=TC.getParam("Step3Value_"+i.toString())
```
![mlt1md_clickonfirstlink](https://cloud.githubusercontent.com/assets/10678180/8502680/53e360f0-2179-11e5-9cc1-b96e96c25486.png)

 6.Click on the first link .

![mlt1md_secpops](https://cloud.githubusercontent.com/assets/10678180/8502717/08af42e2-217a-11e5-915f-5e8e5c0f696a.png)

This section pops up.

![mlt1md_step3val](https://cloud.githubusercontent.com/assets/10678180/8502772/b4197c9c-217a-11e5-96c6-eb77cc41dfb5.png)

 7.Replace the Name field with Step3Value

![mlt1md_changeidmethos](https://cloud.githubusercontent.com/assets/10678180/8502808/28bcfa56-217b-11e5-8e8f-22d1b2311054.png)

 8.Change the ID Method to JavaScript by clicking drop down menu.

![09mlt1md_replacejs](https://cloud.githubusercontent.com/assets/10678180/8501821/e2f9af66-216e-11e5-83eb-0c2dab09e894.PNG)

 9.Replace the JavaScript field with the below code by clicking on JS.

```
var xpath="//input[@type=\"checkbox\" and @value=\""+ArgsContext.Step3Value+"\"]"
evalXPath(xpath);
```

![10mlt1md_delete](https://cloud.githubusercontent.com/assets/10678180/8501823/ead42e6e-216e-11e5-8639-a8f659683496.PNG)

![11mlt1md_delete2](https://cloud.githubusercontent.com/assets/10678180/8501825/eea8a7ea-216e-11e5-8edf-4450104e8676.PNG)

 10.Finally, select in stock steps and delete one by one by performing right click and delete technique.

 11.Save the script and Run.
