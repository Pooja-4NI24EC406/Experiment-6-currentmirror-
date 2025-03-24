

# Experiment-6-currentmirror
<h1>CURRENT MIRROR</h1>     
<p> In the IC,the Mosfet amplifiers are baised using the CURRENT SOURCE. Typically in the IC's this current mirror is used as a current source. The main advantage of the baising the amplifier with the constant current is that it provides high voltage gain and it also improves the baising stability.</p>
<h3><b>CONTENTS</b></h3>
<br><b>THEORY</b>
<br><b>WORKING & APPLICATIONS</b>
<br><b>AIM OF THE CIRCUIT</b>
<br><b>REQUIRED COMPONENTS with there SPECIFICATION</b>
<br><b>LTSpice SIMULATION</b>
<br><b>CALCULATION AND COMPARION TABLE</b>
<br><b>Result, Inference, conclusion</b>

<h3><b>THEORY</b></h3>
<br>The current mirror is an analog circuit that senses the reference current and generates the copy or number of copies of the reference current, with the same characteristics. The replicated current is as stable as the reference current source. The replicated current could be the same as the reference current (Icopy = IREF), or it could be either multiple or fraction of the reference current.

<br>A current mirror can also be implemented using MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors).
<br>Instead of BJTs, two identical MOSFETs (M1 and M2) are used.
<br>The drain of M1 is connected to its gate, forcing it into saturation mode, where it acts as a constant current source.
<br>The gate of M1 is connected to the gate of M2, ensuring that M2 also operates in the same conditions as M1. The output current I_OUT is then mirrored from I_REF.
<br>The reference current is given by the MOSFET saturation current equation:Iref=1/2kn(w/L)Vov^2


![image](https://github.com/user-attachments/assets/f7bc1780-deb8-42f6-8ee8-711e1b93b35d)


<h3><b>Why Current source</b></h3>
Current Mirrors are particularly useful in the integrated circuits, for biasing the amplifiers. The advantage of biasing the amplifiers with the current source is that it provides a high voltage gain and good biasing stability. This current source can be generated using a simple PMOS transistor or using a MOS transistor in cascode configuration (to achieve higher gain) as shown in figure

![image](https://github.com/user-attachments/assets/f6266441-6905-4fd3-b473-c9703af54836)



But this type of MOS current source  is susceptible to the change in the biasing voltage and the change in temperature. Moreover, the integrated circuit may contain hundred or thousand of such amplifiers. To bias all the amplifiers with precise biasing voltage is another challenge. So, to overcome all these problems, in integrated circuits, one stable current source is fabricated within IC, and using the current mirror the multiple copies of the stable current source is generated (which can be used to bias the amplifiers)

<h3><b>MOSFET- Current Mirror</b></h3>
It shows a current mirror circuit using the NMOS transistor. The reference current is converted to the voltage using diode connected transistor and the same is applied between the gate and the source of the another MOSFET.


![image](https://github.com/user-attachments/assets/70a75796-f56b-4378-8f57-924361d8297c)

<br>The relation between the ID1 and IREF can be given by the expression Id1=((w/l)1/(w/l)ref)Iref

By changing the W/L ratio of the two transistors, the current which is fraction or multiple of the reference current can be generated. The only thing which needs to be ensured is that, the MOSFET should operate in the saturation region.

<h3><b>Effect of Channel Length Modulation on Current Mirror</b></h3>
So far during the discussion, the effect of channel length modulation was neglected. If the channel length modulation effect is also considered, as the drain to source voltage (VDS) of the MOSFET increases, the drain current also slightly increases.

<br>Considering the channel length modulation effect, if VDS of MOSFET M1 changes by ΔVDS then the drain current ID1 also changes to ID1 + ΔID1. 

![image](https://github.com/user-attachments/assets/814fc7d4-47a7-40e1-b1cd-427b9027c39c)

<br>The effect of channel length modulation can be reduced by increasing the length of the channel for the given W/L ratio.

![image](https://github.com/user-attachments/assets/5584fcc9-f40d-4396-919b-5c47c0585e5c)

<h3><b>PMOS Current Mirror</b></h3>
It shows the implementation of current mirror using the PMOS transistors. In PMOS current mirror, the source terminals for both transistors are connected to Supply voltage Vdd.

![image](https://github.com/user-attachments/assets/9115b085-bc37-4da3-905d-9bcbe34ad911)

<h3><b>APPLICATIONS</b></h3>
<br>Biasing circuits
<br>Analog signal processing
<br>voltage references
<br>digital to analog converter
<br>operational amplifier
<br>sensor circuits



<h3>AIM</h3>
<b>Design and analyze current mirror circuit as active load in amplifier circuit</b>

<br><b>Circuit daigram1</b>

![image](https://github.com/user-attachments/assets/d78da15e-9d51-4c8b-b3c1-73b958d48fff)


<br><b>1.</b> Design for Av>-10v/v, VDD=1.8v, P<=1mw
<br>Itotal=P/VDD   and  Itotal=Iref+Ix
<br>design for the current mirror ratio----> 1:1 and 1:2 
<br><b>2.</b>Analyze the circuit current mirror--->DC analysis
<br><b>3. case1:a)</b>Lmin=180nm      (W/L)=x
           <br> <b>b)</b>l=500nm     (W/L)=x
          <br> <b>c)</b>L=1um       (W/L)=x
<br>Avalyze the current mirroring maintain (W/L) same as first design
<br><b>4.</b>Transient and AC analysis
<br> Maximum output swing
<br>BW

<br><b>Vary the current mirror ratio and analyze the current copying/mirroring</b>

<b>Circuit daigram 2</b>

![image](https://github.com/user-attachments/assets/2e480a47-2a14-4beb-bc18-3c8dadcbd15a)

Design the differential Amplifier using the same design specification as experiment 3 ---> differencial amplifier, Perform DC analysis, transient analysis and AC analysis

<h3><b>REQUIRED COMPONENTS with their SPECIFICATION</b></h3>

| *Component*   | *Label* | *Specification/Description* |
|---------------|----------|----------------------------|
| *MOSFETs*   | M1, M2  | Matched PMOSFETs for current mirroring |
| *MOSFET*    | M3      | Acts as an active load (common source amplifier) |
| *Power Supply* | VDD | 1.8V  |
| *Current Source* | I_ref | Reference current source |
| *Input voltage* | Vin 0.5V| Used for biasing (values depend on design) |

<h3><b>LTSpice simulation</b></h3>
<br><b>DESIGN FOR THE CURRENT MIRROR RATIO 1:1</b>

<h4><b>CIRCUIT DAIGRAM 01</b></h4>

![image](https://github.com/user-attachments/assets/05cecad0-c296-434b-9147-f43f1ab4db4b)

   
<br>M1 Lenght= M2 Lenght= 180nm
<br>M1 Width=10um and M2 Width = 10um (bcz for 1:1 ratio)

<h4><b>DC Analysis</b></h4>



<br>Vout=VDD/2
<br>   =1.8/2=0.9V(Theoritically)
<br>From DC Analysis
<br>

<br>Vout= Vx
<br>Itotal=Iref+Ix
<br>Iref=
<br>Ix=
<br>Iref=Ix
<br> we can observe that PMOS are diode connected so by inspection it is working in saturation region



<h4><b>TRANSIENT ANALYSIS</b></h4>

![image](https://github.com/user-attachments/assets/d56792e4-4407-4b36-af3c-b8d29a13bfdd)



<br>The Vin is given as DC offset value that is 0.526,20m,1K hz frequency so for that values we can observe the <b>output voltage is 1.5V</b>

<h4><b>AC ANALYSIS</b></h4>

![image](https://github.com/user-attachments/assets/214e61fe-bd11-49e1-baab-84e917dd1a4d)



<br>The GAIN from the LTSpice simulation of this circuit is 29.5dB
<br>29.5-3=26.5dB
<br>BANDWIDTH=FH-FL
<br>BANDWIDTH=756.67MHz


<br><b>DESIGN FOR THE CURRENT MIRROR RATIO 1:2</b>
<h4><b>CIRCUIT DAIGRAM 02</b></h4>


<br>M1 Lenght= M2 Lenght= 180nm
<br>M1 Width=10um and M2 Width = 20um (bcz for 1:2 ratio)

<h4><b>DC Analysis</b></h4>



<br>Vout=VDD/2
<br>   =1.8/2=0.9V(Theoritically)
<br>From DC Analysis
<br>

<br>here Vout is less than Vx
<br>Itotal=Iref+Ix
<br>Iref=
<br>Ix=




<h4><b>TRANSIENT ANALYSIS</b></h4>




<br>The Vin is given as DC offset value that is 0.526,20m,1K hz frequency so for that values we can observe the <b>output voltage is 1.5V</b>

<h4><b>AC ANALYSIS</b></h4>



<br>The GAIN from the LTSpice simulation of this circuit is 29.5dB
<br>29.5-3=26.5dB
<br>BANDWIDTH=FH-FL
<br>BANDWIDTH=756.67MHz


<br><h3><b>Analyze the current mirroring maintaining (W/L) same as first design</h3>
<br>L=500nm
<h4><b>CIRCUIT DAIGRAM 03</b></h4>

   
<br>M1 Lenght= M2 Lenght= 1um
<br>M1 Width=10um and M2 Width = 10um (bcz for 1:1 ratio)

<h4><b>DC Analysis</b></h4>



<br>Vout=VDD/2
<br>   =1.8/2=0.9V(Theoritically)
<br>From DC Analysis
<br>

<br>Vout= Vx
<br>Itotal=Iref+Ix
<br>Iref=
<br>Ix=
<br>Iref=Ix




<h4><b>TRANSIENT ANALYSIS</b></h4>




<br>The Vin is given as DC offset value that is 0.526,20m,1K hz frequency so for that values we can observe the <b>output voltage is 1.3V</b>

<h4><b>AC ANALYSIS</b></h4>



<br>The GAIN from the LTSpice simulation of this circuit is 29.5dB
<br>29.5-3=26.5dB
<br>BANDWIDTH=FH-FL
<br>BANDWIDTH=756.67MHz



<br>L=500nm
<h4><b>CIRCUIT DAIGRAM 01</b></h4>

   
<br>M1 Lenght= M2 Lenght= 500nm
<br>M1 Width=10um and M2 Width = 10um (bcz for 1:1 ratio)

<h4><b>DC Analysis</b></h4>



<br>Vout=VDD/2
<br>   =1.8/2=0.9V(Theoritically)
<br>From DC Analysis
<br>

<br>Vout= Vx
<br>Itotal=Iref+Ix
<br>Iref=
<br>Ix=
<br>Iref=Ix




<h4><b>TRANSIENT ANALYSIS</b></h4>




<br>The Vin is given as DC offset value that is 0.526,20m,1K hz frequency so for that values we can observe the <b>output voltage is 1.3V</b>

<h4><b>AC ANALYSIS</b></h4>



<br>The GAIN from the LTSpice simulation of this circuit is 29.5dB
<br>29.5-3=26.5dB
<br>BANDWIDTH=FH-FL
<br>BANDWIDTH=756.67MHz











  

