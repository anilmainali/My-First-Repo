

## Narration for Auto Correlation.

We want to record into a Web protocol script.

We go to **Recording Options.** Instead of generating **C programming** we want to generate **JavaScript program code.**

So change the Language to **JavaScript** from default **C**.

By default, correlation methods are enabled for all LoadRunner users. Change/tweak correlation settings in Recording Options dialog. Automatic correlations are enabled/disabled by selecting the **‘Correlation Scan’** checkbox under **General > Code Generation.**

To define preferred settings go to **Correlations >Configuration node.** We need to have all scan options checked. 

We need to have the server running In Windows 7, click the Windows key and drill down into all programs, HP Software .The sample app runs as localhost, without connecting to the internet.

We can now click the **red icon** to begin recording.

Login as “jojo” with password “bean”. Click “Sign Off”, then **Stop** recording.

When code generation is done, The **Correlation Studio (Design Studio)** is shown.

Review the dynamic values.

Now Replay the script and we can observe that the script has failed. 

To understand why the script has failed let’s check the **Run-Time viewer.**

The script has failed because of **bad session value.**

Now click on the **Design Studio.**

```
Design Studio enables you to manage dynamic values detected by all correlation scans in the unified form and provides the complete information about the location, extraction method and the expected replacements in the script. 
```


Review the dynamic values. We can observe that there is a userSession value.

Select the field and click on **Correlate.** Observe the status is checked green and the correlation has been applied.

Look in the script and observe the correlation has been applied and the userSession value has been changed with a parameter.(userSession)

Replay the script one more time and this time the script is passed.

Just to confirm check the **Run-Time viewer** to see if all responses are coming back as expected.

This is one of the way how we **auto correlate** the dynamic value using **Design Studio.**

