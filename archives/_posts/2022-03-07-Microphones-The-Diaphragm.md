---
title: 'Microphones: The Diaphragm'
categories:
  - 手札
tags:
  - 手札
  - 轉錄
date: 2022-03-07 14:05:01
---
<br>
<center>{% asset_img title.jpg title %}</center>
<br>

{% link 原文連結 https://www.thebroadcastbridge.com/content/entry/17257/microphones-part-4-microphone-technology-the-diaphragm %}

### Most microphones need a diaphragm in order to follow some aspect of the air motion that carries the sound.

The diaphragm must have a certain mass, and in order to be able to move it must be supported by something compliant. The result is an unavoidable problem, which is that when any time mass and compliance are seen together there will be resonance. Exactly the same problem is seen in the suspension of an automobile, the blades of a helicopter and in the diaphragm of a loudspeaker. The mass and the compliance must be accompanied by damping if movement at resonance is not to be uncontrolled.

The motion of a diaphragm can be considered in terms of its displacement or position, its velocity or its acceleration. As will be seen, in practice all three are relevant. Fig.1 shows the relationship between them at a single frequency. When the frequency changes, each way of considering motion has a frequency response and the responses are 6dB/octave apart.

{% asset_img fig1.png fig1 %}
Fig.1 Any resonant system can be described by the displacement, velocity or acceleration. The relationship between them at a single frequency is shown here.

If we have a flat amplitude response, the velocity response will rise at 6dB/octave and the acceleration will rise at 12dB/octave. Whilst the mass, the stiffness and the damping of the moving system all have an effect, at certain frequencies one of them is dominant.

At frequencies below resonance, the mass and the damping have little effect and what happens as a result of an applied force is dominated by the stiffness. In other words if the moving system were replaced by a spring having the same stiffness as the diaphragm, the response would be much the same. It's a characteristic of the stiffness control region on the left side of Fig.2a) that the amplitude of the diaphragm motion is independent of frequency.

We could make a microphone by putting the resonant frequency at the top of the audio band and the diaphragm would have a flat amplitude response.

Using plenty of damping, it would be possible to flatten the response of Fig.2b) such that the resonance could be in the center of the audio band and the system would have a flat velocity response.

Fig.2c) shows that above resonance, the stiffness and the damping have little effect. The moving system can be replaced by an equivalent mass that acts like an integrator. Simple inertia makes a mass harder to move as frequency rises, so the response falls with frequency in the mass control region, which is also a region of constant acceleration. Some microphones and all moving coil loudspeakers work in this region where the audio band is placed above the fundamental resonance.

What Fig.2 is effectively showing is that there are three different ways of locating diaphragm resonance in a transducer with respect to the audio band and each one has a different characteristic frequency response. That might appear to cause some problems, but it turns out that the various transduction methods we have also display different frequency responses, and the overall response of the microphone, which is what matters, is the sum of the two responses. In other words some transduction principles naturally fit well with certain locations of the resonant frequency.

An omni-directional microphone is effectively a fast-acting barometer as it considers only the scalar pressure of the sound. A pressure sensor can be made by stretching a diaphragm across an aperture in an otherwise sealed container. In practice the sealing would be less than perfect to allow the microphone to survive changes in the weather and transport by air. Altimeters and barometers differ only in the way the scale is printed.

The motion of such a diaphragm could easily be measured by making it one plate of a capacitor or condenser. It is a characteristic of variable capacitance transducers that they work on the position of the diaphragm. In other words they have a flat frequency response with respect to the amplitude of the diaphragm motion.

Referring back to Fig.2a), if the diaphragm is light and placed under a lot of tension, the resonant frequency can be placed at the top of the audio band so the diaphragm is working under stiffness control and the amplitude response is flat. The flat mechanical response of the stiffness-controlled diaphragm combined with the flat response of the capacitive transduction system gives a microphone with a theoretically flat frequency response, so this is a commonly found combination.

{% asset_img fig2.png fig2 %}
Fig.2 In the stiffness control region shown at a) the diaphragm amplitude is independent of frequency and the velocity is proportional to frequency. In the mass control region shown at b) the system has constant acceleration and in the damping control region at c) the system has constant velocity.

In contrast, a ribbon microphone is designed to have a figure-of-eight polar diagram. It does that by acting purely on the air velocity, which is directional and ignoring the scalar air pressure. Sound arriving in the plane of the ribbon has the same effect on both sides, so there is no resultant ribbon motion. That is what happens in the null of the response.

Sound arriving from other angles reaches the two sides of the ribbon at a slightly different time, so effectively the ribbon sees the difference between the two versions of the sound. The ribbon is differentiating the waveform, which is why it is also called a gradient microphone. The steeper the waveform becomes, the bigger the gradient.

The ribbon moves in a magnetic field, and the laws of electromagnetism say the voltage generated is proportional to the velocity of the ribbon. That means the frequency response of the transduction system rises at 6dB/octave. The solution is simple. We just put the resonant frequency of the ribbon at the bottom of the audio band, so the ribbon works in mass control. Fig.2b) shows that the diaphragm velocity falls at 6dB/octave, so when we combine that with the rising characteristic of the electromagnetic generator we get a flat frequency response.

This is precisely the mirror of the operation of the moving coil loudspeaker of Rice and Kellog. Sound radiation of a diaphragm is proportional to acceleration. By making the diaphragm mass-controlled there is a falling mechanical response to compensate for the rising acoustic response.

The microphone and the loudspeaker are essentially the same thing but optimized to work in different directions. However, in extreme applications, such as recording large and powerful drums, a low frequency loudspeaker makes quite a good microphone as it not likely to suffer any damage from exposure to high SPL and it will naturally filter out high frequencies. A speaker in a sealed enclosure will have better phase linearity than one in a ported enclosure.

The cardioid microphone must combine the directivities of figure-of eight and omni-directional units. The reversed phase at the rear of the figure-of-eight response causes it to null with the omni response. Initially, cardioid microphones contained two capsules, one of each directivity, mounted one above the other, but it was difficult to make the two microphone signals add and subtract properly, especially for sounds arriving from above or below the plane of the microphone.

The solution is to construct a single microphone that has the attributes of both omni and figure-of-eight types. This is harder than it sounds, because as was seen above, a typical velocity microphone works in mass control whereas an omni microphone works in stiffness control.

{% asset_img fig3.png fig3 %}
Fig.3 In the cardioid microphone the back of the diaphragm has an acoustic delay. At a), sound from the front experiences two delays D1 and D2 before it reaches the back of the diaphragm. When sound approaches from the rear, at b) the delays are in parallel and cancel out.

A diaphragm suspended in free air cannot respond to air pressure changes because they will be applied to both sides equally. Such a microphone can only respond to air velocity if the sound can be sampled at two locations between which is a gradient. In the cardioid microphone, access to one side of the diaphragm has been modified by the addition of an air cavity and an acoustic resistance, which together cause a delay to sound approaching the rear of the diaphragm.

The diaphragm now sees sound pressure on the outside and delayed sound pressure on the inside and responds to the difference. The diaphragm has become a gradient microphone.

With careful geometric design, the delay becomes a function of direction. Sound approaching from ahead, as shown in Fig.3a) experiences two delays before it reaches the back of the diaphragm; one due to the depth of the outside of the capsule D1 and one due to the internal delay D2. The gradient effect is then strongest and the sensitivity of the microphone is the greatest.

On the other hand, sound approaching from behind as in Fig.3b) sees the two delays in parallel, and arrives at the same time on both sides of the diaphragm, so there is no gradient effect and no response. That corresponds to the null at the rear of the cardioid response.

Sound approaching from 90 degrees reaches the outside of the diaphragm directly but reaches the inside through one delay. The gradient effect is halved.

This principle is used in the majority of hand-held microphones supplied for public address and sound reinforcement. The non-acoustic requirements of such a microphone include surviving rough handling, functioning in the high humidity due to the performer's breath and being immune to interference from e.g. stage lighting. The moving coil principle has shown itself to be more than adequate to meet those requirements.
