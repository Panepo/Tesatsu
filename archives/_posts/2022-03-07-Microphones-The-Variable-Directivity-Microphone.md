---
title: 'Microphones: The Variable Directivity Microphone'
categories:
  - 手札
tags:
  - 手札
  - 轉錄
date: 2022-03-07 14:10:25
---
<br>
<center>{% asset_img title.jpg title %}</center>
<br>

{% link 原文連結 https://www.thebroadcastbridge.com/content/entry/17354/microphones-part-5-the-variable-directivity-microphone %}

### The variable directivity microphone is very popular for studio work. What goes on inside is very clever and not widely appreciated.

The variable directivity microphone has the advantage that it largely replaces a box full of fixed-response units and the directivity can be changed in an instant. The variable directivity microphone emerged from work in the 1930s carried out by von Braunmuhl and Weber of Neumann. These two went on to develop high frequency bias that made magnetic tape viable for sound recording. Their microphone work is of the same importance to audio as the work done by Rice and Kellog on loudspeakers.

{% asset_img fig1.png fig1 %}
Fig.1 - The central plate has a diaphragm mounted on both sides. Transverse drillings allow damped airflow between the sides in gradient operation.

Fig.1 shows that these devices have two diaphragms, one on each side of a central plate that is drilled in a peculiar fashion with some holes going right through and some not. Unlike a hand-held microphone, which is intended to accept sound axially in the so-called end-fire configuration, the dual diaphragms of the variable directivity microphone require a side-fire construction where the microphone is oriented transversely to the sound source.

The sensitive side of the microphone when used as a cardioid will be denoted by a small mark on the relevant side, or by a small LED.

It is important to appreciate that the variations of pressure in sound could not take place if particles of air were unable to move closer together or further apart, so the velocity changes and the pressure changes of sound are inseparable. In a variable directivity microphone the two diaphragms are responding to both aspects of the sound at all times. The response to each is different.

If the system is exposed to sound travelling in a direction normal to the diaphragms, the presence of the diaphragm assembly causes a pressure gradient that will be sensed equally and in the same phase by both diaphragms. They will move in response to the pressure gradient and air will flow through the open drillings in the central plate, permitting that movement.

The diaphragm tension is arranged to place the resonance in the center of the audio band so that the motion of the diaphragm is stiffness controlled, but the drillings in the center plate act as viscous dampers to air movement, so the diaphragms operate with a high damping factor. The resistance-controlled diaphragms effectively move in tandem and are sensing velocity, which is just what is required.

If the assembly is turned by 90 degrees, the gradient disappears because the particle velocity is parallel to the diaphragms. The system therefore displays a figure-of-eight response.

If the response to pressure is considered, it must be recalled that pressure is a scalar quantity and acts identically in all directions. If the system is exposed to increasing pressure on the positive half cycle of a sound wave, both diaphragms will see the same pressure and both will react in the same way by tending to move inwards towards one another. The diaphragm movement in response to pressure is mechanically out of phase.

The system is completely symmetrical to pressure, so when one diaphragm tries to push air through the cross-drillings in the center, it finds the other diaphragm is trying to do exactly the same thing so the two effects cancel. There is no net air movement in the cross drillings as a result of pressure changes. Essentially the air under the diaphragms has nowhere to go and so it acts as a relatively stiff compliance, causing the resonant frequency of the diaphragm to be high.

{% asset_img fig2.png fig2 %}
Fig.2 - Typical internal wiring of variable directivity microphone changes the polarizing voltages on one of the two diaphragms.

The diaphragms are then stiffness controlled and work in constant displacement, which are the ideal conditions for variable-capacitance sensing. As the diaphragm tension is determined by the requirements of velocity mode, the resonant frequency in pressure mode can be adjusted by the partial drillings. Increasing the volume of those drillings will reduce stiffness.

Essentially in the variable directivity microphone we have two variable capacitors that are changing according to the sound arriving. The traditional way of connecting them up is shown in Fig.2.

The microphone contains a polarizing power supply running from a battery, or from phantom power, and a potential divider puts the voltage of the center plate at the mid point of the polarizing voltage. The front plate is typically polarized from the negative of the supply. However the rear plate can be provided with a range of voltages using a switch and resistors or using a variable resistor.

If the front and rear diaphragms receive the same polarizing voltage, their output will be in-phase for pressure changes and if the diaphragm voltages are summed, the result will be an omni-directional response. However, if the rear diaphragm is supplied with a polarizing voltage opposite to that of the front diaphragm, the pressure signals will cancel and the velocity signals will be in-phase. The result will be a figure-of-eight response.

If the rear diaphragm is not supplied with a polarizing voltage, the front diaphragm will see a sum of pressure and velocity signals and the result will be a cardioid response.

More recent microphones may adopt the structure of Fig.3. Two amplifiers are used, one summing the motion of the diaphragms and one amplifying the difference. The microphone simultaneously outputs pressure and velocity signals and if both are recorded, the directivity of the microphone can be determined in post-production.

{% asset_img fig3.png fig3 %}
Fig.3 - A later type of microphone, in which the pressure and gradient signals are output separately.

Fig.4 shows some sound energy expanding away from a source. Under normal conditions, the area over which the sound energy is spread increases as the square of the distance. This is where the famous inverse square law comes from. A couple of things follow from this expansion. One is that a point source of sound cannot exist. If it did the intensity there would be infinite. All real sources of sound have finite size.

Another thing that follows is that the spherically expanding sound has a built in gradient effect acting radially. A diaphragm facing the sound source sees an additional gradient because the intensity on the source side of the diaphragm must be greater than the intensity on the far side.

The effect depends on the size of the diaphragm and the radius of curvature of the wavefronts, but not on frequency. As a microphone is brought closer to a sound source, at some point the gradient due to the spherical wave exceeds the gradient due to particle velocity. Any closer and we may have a problem. Further away, the radius of the spherical wave is so great that it doesn't really differ from a plane wave.

Gradient microphones differentiate the sound waveform, which means the force on the diaphragm rises with rising frequency. This is compensated inside the transducer, which has a response that falls with rising frequency, using, for example mass control.

The transducer of a gradient microphone is designed to compensate for a diaphragm force that rises with frequency. The force due to wave front curvature doesn't rise with frequency and the result is that the transducer unwittingly boosts the low frequencies due to wave front curvature. The result is the classic bass tip-up demonstrated by all gradient microphones, but not by pressure microphones.

Given that the figure-of-eight microphone relies totally on gradient whereas in the cardioid only half of the output comes from gradient information it is not surprising that cardioids show half as much bass tip-up as figure-of-eights. Pressure sensing, or omni, microphones cannot display bass tip-up at all because they cannot sense velocity.

{% asset_img fig4.png fig4 %}
Fig.4 - Inverse square sound propagation implies there must be a velocity gradient away from the source.

One sometimes reads that dual-diaphragm or variable directivity microphones display bass tip-up when set to an omnidirectional response because they essentially contain two cardioid microphones. This is a complete fallacy. Whilst a variable directivity microphone certainly can be thought of as containing two cardioids it is necessary to remember a few of salient facts:

Firstly the two cardioids are facing in opposite directions and any wave front curvature seen by one will be precisely reversed and cancelled out in the other. Secondly, the act of adding the two opposite-facing cardioid responses cancels out the gradient information. Perhaps the most compelling fact is that in real life, variable directivity microphones set to omni simply don't display the proximity effect.

Given the universality of the cardioid microphone for public address it follows that bass tip-up is also near universal and compounded by the use of reflex loudspeakers to give that boomy, muddy character to most amplified sound. Any hand-held cardioid microphone needs to be followed by a 6dB/octave bass cut filter set to a surprisingly high frequency.

If a microphone of the type shown in Fig.3 is available, in which the pressure and gradient signals are both available, it is possible to combine the two signals in various way. For example if the signals are filtered before addition, the directivity of the microphone can be made frequency dependent. It then becomes possible to implement cardioid and figure-of-eight responses over most of the audio band, but changing to omni response at low frequencies in order to eliminate the proximity effect.

