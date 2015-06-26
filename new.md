## Add Verification

Some applications do not return the correct page and the applications can change. So test scripts ideally would confirm that it got back the page that it expected.

In TruClient Action.

![toolb](https://cloud.githubusercontent.com/assets/10678180/8372687/5081ce02-1bab-11e5-92d9-3456ea6463ca.PNG)

1. Open the **Toolbox** tab at the right edge of the TruClient Sidebar by clicking it.

![funver](https://cloud.githubusercontent.com/assets/10678180/8372722/8bf275fe-1bab-11e5-9f13-3754cfcad8f1.PNG)

2. In the **Functions** tab, drag **Verify** immediately under the web request line.

![vistext](https://cloud.githubusercontent.com/assets/10678180/8372244/fd6a7614-1ba6-11e5-8e74-11ad1f83a647.PNG)

3. In the Property field type "Visible Text", including quote marks around the property name.

![verify](https://cloud.githubusercontent.com/assets/10678180/8372159/2e643620-1ba6-11e5-83d3-186fa24e28bd.PNG)

4. Click on Click to choose an object.

![highlightobject](https://cloud.githubusercontent.com/assets/10678180/8372170/3bc0ff24-1ba6-11e5-95c9-1558312837ac.PNG)

5. Position cursor to highlight (in Green) the control containing the text to be validated.

![highlightgreen](https://cloud.githubusercontent.com/assets/10678180/8372172/4098a3e4-1ba6-11e5-93c0-f14c6834b0b8.PNG)

6. Click on the control (when it's in green) to generate this code:

![verifiedobject](https://cloud.githubusercontent.com/assets/10678180/8372173/44bbc686-1ba6-11e5-98c7-c9459b48d3ee.PNG)

Follow the above technique for the remaining steps to confirm that it got back the page that it expected.