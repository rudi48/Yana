**Yana Operations**

**K1TRB T. Berger (c)4/2016**


**I. The HOME Screen**

**HOME**

The screen below is called the **HOME** **Screen**. The top row is called the **Command Line**. Other rows are called **Frequency Lines**. The HOME screen is shown with several possible choices.

Suppose we wish to sweep a 30MHz (High Frequency) antenna low pass filter over Yana's entire range, measuring to find spurious responses and low attenuation. The leftmost screen sweeps Yana's entire range using the Scalar Network Analyzer (SNA) instrument with frequencies indicated (S) in Start/Finish fashion. The grid (10) will have 10db steps, and Yana is in the run (R) mode. The Start Frequency is 50,000Hz and the Finish Frequency is 70,000,000Hz. A Left Marker is placed at 14.04MHz and a Right Marker at 56.01MHz: 1/4 way through the range. Yana is using the SNA instrument, showing Start/Finish frequencies, with 10db steps on the graph. Yana is ready to run the sweep.

Suppose next we wish to measure the response of an 80m bandpass filter, including responses at the band edges and the skirts of the filter up to 1.25MHz from the center of the band. The second screen shows Yana in SNA mode, with frequencies (C) in Center/Radius fashion. The graph is set (3) to have grid steps of 3db. Yana sweeps the 80m band from 2.5MHz to 5MHz, (centered at 3.75MHz with radius 1.25MHz each way from this center) with markers at 3.5MHz and 4.0MHz (distance 250KHz each way from the center): the band edges. Further, Yana is ready to run (R).

Now check a 40m dipole for its SWR over the band with the SWR Bridge mounted on Yana. The third screen shows Yana ready to sweep a 40m antenna with the SWR instrument (technically, Yana computes VSWR). The SWR instrument is selected in (S) Start/Finish fashion, beginning at 7MHz and ending at 7.3MHz. The grid (1) will have SWR 1 steps. Markers are set at 7.1MHz and 7.2MHz. Yana is set to run (R).

Suppose we wish to find the 3db points of a 8.138MHz crystal filter of 2.8KHz nominal bandwidth by measuring power through the filter. The 3db/60db shape factor is supposed to be 2:1 so the 60db bandwidth should be 5.6KHz. The radius from the center frequency would be 2.8KHz (half the 2:1 bandwidth). The radius to the bandwidth edges should be half the expected 3db bandwidth: 1.4KHz, so markers are placed there.

The DDS in Yana is independent of the power detector. Therefore it is left running and tunable when in the Power (PWR) instrument. Feeding the DDS to the filter enables output to be measured using the PWR instrument in Yana. The DDS output is falling throughout its range but is fairly constant over a 5.6KHz range around 8MHz. If there is concern, the power meter instrument (PWR) in Yana will measure the DDS output at any frequency either through the filter or directly.

Record the filter response at the center of the filter: 8.138MHz. Tune either side of center until the output falls 3db.

The fourth screen shows Yana set to the power meter (PWR) instrument. The frequencies (C) are set for Center/Radius. There is no graph so no graphing dimensions (\_ \_) are given, and Yana's operation is set to run (R). The center frequency is 8.138MHz, the radius is 2.8KHz: tuning will be in this range. The markers are set either side of center at 1.4KHz but they have no relevance so could be set arbitrarily.

**Instrument Field Start/Center Field Graph Field Operation**

**SNA SWR PWR S C 10/3 1/.5 \_ \_ R C S**

(R) in the Operations position means Yana is ready to run. (C) means Yana is ready to calibrate, and (S) means Yana is ready to save the current state. Each time Yana starts, the saved state is the starting point.

**HOME Position**

The HOME screen is showing, R is in the upper right corner, and the cursor is on R.

**Buttons**

Click: Depress and release the button quickly.

Push: Depress the button until the screen goes black.

Hold: Depress the button until the screen goes black and then the HOME screen reappears.

Turn: Turn the knob.

**Button Actions**

A Hold always returns Yana to the HOME position with the following exception:

a Hold in the HOME position executes the command set up by the Home Screen.

**The Button on the HOME Screen**

Click:

> Move the cursor along the selected row. (On a frequency, it sets the decade \[stepping in 100’s\] for tuning. On the Command Line clicking moves from field to field.)

Push:

> Advance to the next lower line except on the bottom line. From the bottom line, Push sends the cursor to the Center or Start Frequency Line.

Hold:

> Returns to the HOME position with the run (R) operation set except when already in the HOME position. In the HOME position, Hold executes the command.

Turn:

> On a Frequency line, the frequency tunes according to the cursor location. (Click to change that.) Clicking moves the cursor two positions to the right (or cycles back to the Mhz position).
>
> On the Command Line, turning selects the possibilities for a command (instrument, frequency fashion, graphing dimension, or operation). Commands do not cycle so the knob must be turned the other way when at the end of choices.

**Note:** Yana operates as follows. When the knob is turned, an interrupt records the change. This change is not immediately noted. As Yana checks tasks, eventually the accumulated knob turning is recorded and displayed. The occasional checking is called “polling.” That is, the rotation is recorded immediately by an interrupt but Yana only notes it when the possibility of a rotation is polled.

The button is always polled. In other words, Yana can only notice if the button is being pushed if she checks the button while it is down. Normally this is not a problem since computers are fast and humans are slow. However, in the PWR mode, the button is sluggish because Yana only checks when not doing other things and those other things take noticeable time.

**II. The SNA Graphing Screen**

Yana sweeps the range and graphs the readings. Two vertical steps are set on the HOME screen: 10db or 3db. The top of the screen is 0db and the bottom is either -21db or -70db.

|                    |                   |
| ------------------ | ----------------- |
| **Graphing Range** | **Vertical Grid** |
| **70db**           | **10db**          |
| **21db**           | **3db**           |

The Button (Click, Push, Hold) has no effect on graphing. **Turn the knob to stop graphing.** Continuous graphing is useful for real-time tuning (e.g. an antenna coupler or a bandpass filter).

Click: Nothing. xxx

Push: Nothing. xxx

Hold: Nothing. xxx

Turn: The graph stops and data are displayed. Yana is now in a slightly different mode: **SNA Graphing Data Mode**.

The following table shows the SNA graphing data displayed in **SNA Graphing Data** mode. Yana is sweeping the full spectrum in SNA mode with the open SWR bridge mounted.

|                |            |             |
| -------------- | ---------- | ----------- |
| **Frequency**  | **db**     | **Meaning** |
| **35,025,000** | **-11.9**  | **Tune**    |
| **19,286,228** | **-12.4**  | **Min**     |
| **50,040**     | **- 9.0**  | **Max**     |
| **14,040,000** | **-12.2**  | **L**       |
| **56,010,000** | **- 11.3** | **R**       |

The first column is the frequency. The second column is the db down at that frequency. The third column is the meaning of the Frequency.

Min: is the minimum reading, the lowest point on the graph.

Max: is the maximum reading, the highest point on the graph.

L: is the reading at the Left Marker.

R: is the reading at the Right Marker.

Turning the knob changes the Tune frequency. Think of the knob as tuning along the curve on the graph. A new reading is taken at the new frequency. Tuning is over the range of the graph, i.e. between the minimum and maximum graphed frequencies. The stepsize for tuning can be changed by clicking the button.

**Note:** When tuning the readings may be different from the SNA graphing data and may change when retuning the same frequency. The graphing values are read from the Detector exactly once and recorded. However, when tuning, the detector is read 8 times then averaged. Even at that, changes with noise, variations in digital conversion, and variability in circuits can cause small changes in a short time. When tuning, a reading is taken each time the knob is turned one click. Between turning clicks, no readings are taken. To see the variations at one frequency, tune back and forth. Yana's precision (number of decimal places shown) exceeds her accuracy (how accurate she really is) so that you can make the choice of what to believe.

**The Button in SNA Graphing Data Mode**

Click: change the tuning step size.

Push: return to continuous graphing.

Hold: go HOME.

Turn: change the **Tuning** frequency.

**III. The SWR Graphing Screen**

Yana sweeps the range and graphs the readings. Two vertical steps are set on the HOME screen: SWR 1 or SWR .5. The top of the screen is 1.0 VSWR and the bottom is either 4.5 VSWR or 8.0 VSWR.

|                    |                   |
| ------------------ | ----------------- |
| **Graphing Range** | **Vertical Grid** |
| **8.0**            | **1.0**           |
| **3.5**            | **0.5**           |

The Button (Click, Push, Hold) has no effect on graphing. **Turn the knob to stop graphing.** Continuous graphing is useful for real-time tuning (e.g. an antenna coupler or a bandpass filter).

Click: Nothing. xxx

Push: Nothing. xxx

Hold: Nothing. xxx

Turn: The graph stops and data are displayed. Yana is now in a slightly different mode: **SWR Graphing Data Mode**.

The following table shows graphing data displayed in **SWR Graphing Data** mode. Yana is sweeping the full spectrum in SWR mode with a 12.5 ohm load mounted on the bridge. In a perfect world, the VSWR should be 4.0.

|                |          |             |
| -------------- | -------- | ----------- |
| **Frequency**  | **VSWR** | **Meaning** |
| **35,025,000** | **3.9**  | **Tune**    |
| **632,916**    | **3.2**  | **Min**     |
| **50,000**     | **8.3**  | **Max**     |
| **14,040,000** | **4.0**  | **L**       |
| **56,010,000** | **5.0**  | **R**       |

The first column is the frequency. The second column is the SWR at that frequency. The third column is the meaning of the Frequency.

Min: is the lowest down reading on the graph: the highest VSWR.

Max: is the highest up reading on the graph, the lowest VSWR.

L: is the reading at the Left Marker.

R: is the reading at the Right Marker.

Turning the knob changes the Tune frequency. Think of the knob as tuning along the curve on the graph. A new reading is taken at the new frequency. Tuning is over the range of the graph, i.e. between the minimum and maximum graphed frequencies. The stepsize for tuning can be changed by clicking the button. The bridge performs best between 1.0MHz and 30MHz. At high VSWR readings, small changes in ADC reading can mean big changes in VSWR. Thus the curve can be jagged because the ADC reads in discrete steps.

Note: xxx the button would be very sluggish (like in the PWR instrument), but could add functionality. But what functionality would be useful?

**The Button in SWR Graphing Data Mode**

Click: change the tuning step size.

Push: return to continuous graphing.

Hold: go HOME.

Turn: change the **Tuning** frequency.

**IV. The PWR Screen**

**WARNING! Do not present the meter with more than +10dbm (10mW or 0.7V ... 100W is 70.7V \[100 times too many volts\]). More may fry the AD8307 and burn out the input circuitry. Use the 40db tap for powers up to 100watts. \[The Hayward, Larkin tap is only good up to 60W.\]**

With the 40db tap, 40db should be added to the dbm reading, watts should be multiplied by 10,000, and volts should be multiplied by 100. If the load on Yana is not 50 ohms resistive, all readings are suspicious.

Yana measures its wide range detector and registers the total power in its total bandwidth. Thus when connected to an antenna, Yana will measure all the power present at every frequency. Yana performs best in a 50 ohm environment when given specific frequencies whose total power has meaning.

The presentation is shown below. The SWR bridge is attached with a 12.5 ohm load.

The Generator is connected through the bridge so that the power is that of the Generator minus the loss through the bridge.

|            |
| ---------- |
| **Power**  |
| -58.0 dbm  |
|            |
| 1.57 nW    |
| 280. uV    |
|            |
| Frequency  |
| 16,000,000 |

The power meter function does not need the generator so the Generator is available for any use. The Generator can be fed directly to the power meter and tuned through its range to determine the power output at any frequency. The Generator can be fed through a filter to the power meter and tuned through the range of the filter. The power of the generator varies between 0dbm and 1.2dbm in the range 50KHz to 14MHz. From there it drops off to about -19dbm at 70MHz.

Do not be deceived by Yana's readings. The AD8307 measures up to 100MHz +-1db. The ADC measures voltage in steps which are about 0.2dbm. An ADC is always +- 1count (or in a 0.4dbm range). Readings are determined by the the voltage regulators on the Nano and AD8307 modules. These are neither high accuracy or super stable. Accuracy is improved by calibrating Yana. Instability causes slight variation in readings.

The precision (number of decimals presented) of Yana always exceeds the accuracy (closeness to true value). This is intentional so that you can make the choice of what a reading means.
