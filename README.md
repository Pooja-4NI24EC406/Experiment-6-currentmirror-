# Experiment-6-currentmirror
<h1>CURRENT MIRROR</h1>     
<p> In the IC,the Mosfet amplifiers are baised using the CURRENT SOURCE. Typically in the IC's this current mirror is used as a current source. The main advantage of the baising the amplifier with the constant current is that it provides high voltage gain and it also improves the baising stability.</p>
<h3><b>CONTENTS</b></h2>
<br>AIM of the circuit</br>
<br>Components required with circuit</br>
<br>Theory</br>
<br>Applications, working principle</br>
<br>Analysis of CD</br>
<br>calculation & comparison tables</br>
<br>Result, Inference, conclusion</br>

<h3><b>THEORy</b>/h3>
<br>The current mirror is an analog circuit that senses the reference current and generates the copy or number of copies of the reference current, with the same characteristics. The replicated current is as stable as the reference current source. The replicated current could be the same as the reference current (Icopy = IREF), or it could be either multiple or fraction of the reference current.

<br>A current mirror can also be implemented using MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors).
<br>Instead of BJTs, two identical MOSFETs (M1 and M2) are used.
<br>The drain of M1 is connected to its gate, forcing it into saturation mode, where it acts as a constant current source.
<br>The gate of M1 is connected to the gate of M2, ensuring that M2 also operates in the same conditions as M1. The output current I_OUT is then mirrored from I_REF.
<br>The reference current is given by the MOSFET saturation current equation:Iref=1/2kn(w/L)Vov^2


![image](https://github.com/user-attachments/assets/f909dcff-137f-41c9-8dbd-7d47b1f94a7f)

<h4><b>Why Current Mirrors are used</b></h3>
Current Mirrors are particularly useful in the integrated circuits, for biasing the amplifiers. The advantage of biasing the amplifiers with the current source is that it provides a high voltage gain and good biasing stability. This current source can be generated using a simple PMOS transistor or using a MOS transistor in cascode configuration (to achieve higher gain) as shown in figure

![image](https://github.com/user-attachments/assets/7b6ea27d-1a86-4f89-903a-c7267eba43e4)


But this type of MOS current source  is susceptible to the change in the biasing voltage and the change in temperature. Moreover, the integrated circuit may contain hundred or thousand of such amplifiers. To bias all the amplifiers with precise biasing voltage is another challenge. So, to overcome all these problems, in integrated circuits, one stable current source is fabricated within IC, and using the current mirror the multiple copies of the stable current source is generated (which can be used to bias the amplifiers)

<h4><b>MOSFET- Current Mirror</b></h3>
It shows a current mirror circuit using the NMOS transistor. The reference current is converted to the voltage using diode connected transistor and the same is applied between the gate and the source of the another MOSFET.










<h3>AIM</h3>
<b>Design and analyze current mirror circuit as active load in amplifier circuit</b>
<br><b>Circuit daigram</b>


<br><b>1.</b> Design for Av>-10v/v, VDD=1.8v, P<=1mw
<br>Itotal=P/VDD   and  Itotal=Iref+Ix
<br>design for the current mirror ratio----> 1:1 and 1:2 
<br><b>2.</b>Analyze the circuit current mirror--->DC analysis
<br><b>3. case1:a)</b>Lmin=180nm      (W/L)=x
<br>             <b>b)</b>l=500nm     (W/L)=x
<br>             <b>c)</b>L=1um       (W/L)=x
<br>Avalyze the current mirroring maintain (W/L) same as first design
<br><b>4.</b>Transient and AC analysis
<br> Maximum output swing
<br>BW

<br><b>Vary the current mirror ratio and analyze the current copying/mirroring</b>

<b>Circuit daigram 2</b>



Design the differential Amplifier using the same design specification as experiment 3 ---> differencial amplifier, Perform DC analysis, transient analysis and AC analysis




  

