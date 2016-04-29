

## Narration

We want to record into a Web protocol script.

We go to **Recording Options.** Instead of generating **C programming** we want to generate **JavaScript program code.**

So change the Language to **JavaScript** from default **C**.

By default, correlation methods are enabled. 

Change/tweak correlation settings in Recording Options dialog. 

Automatic correlations are enabled/disabled by selecting the **‘Correlation Scan’** checkbox under **General > Code Generation.**

To define preferred settings, 
go to **Correlations > Configuration node** 
to have all scan options checked. 

We need to have the server running In Windows 7, 
click the Windows key and type "web tours".
(This is faster than drilling into All programs, HP Software, Samples.)

The nice thing about the WebTours sample app is it runs as localhost, 
without connecting to the internet.

We can now click the **red icon** to begin recording.

Login as “jojo” with password “bean”. 
Click “Sign Off”, then **Stop** recording.

When code generation is done, 
the **Correlation Studio (Design Studio)** is shown because we asked for it.

Some dynamic values found may not need to be correlated.

Let's Replay the script to see if it runs without correlation.

The script failed so yeah, we need correlations. 

To understand specifically why the script failed, 
let’s check the **Run-Time viewer**.

The script has failed because of **bad session value.**

Click on **Design Studio.**

   ```
   Design Studio enables you to manage dynamic values detected by all correlation scans in the unified form and provides the complete information about the location, extraction method and the expected replacements in the script. 
   ```

Review the dynamic values. We can observe that there is a userSession value.

Select the field and click on **Correlate**.
This makes use of files LoadRunner created during recording.

Observe the status is checked green and the correlation has been applied.

Look in the script and observe the correlation has been applied 
and the userSession value has been changed with a parameter.(userSession)

Replay the script one more time.
This time the script should pass.

To confirm, check the **Run-Time viewer** to 
see if all responses comes back as expected.

This is one of the ways we **auto correlate** 
the dynamic value using **Design Studio.**

