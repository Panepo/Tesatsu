---
title: 'Microphones: Design Principles'
categories:
  - 手札
tags:
  - 手札
  - 轉錄
date: 2022-03-07 13:51:18
---
<br>
<center>{% asset_img title.jpg title %}</center>
<br>

{% link 原文連結 https://www.thebroadcastbridge.com/content/entry/17052/microphones-part-2-design-principles %}

### Successful microphones have been built working on a number of different principles. Those ideas will be looked at here.

As sound consists of pressure and velocity variations in air, it follows that the first stage in any microphone must be to have some sort of membrane or diaphragm that follows some aspect of those variations.

The next step is to convert the motion of the diaphragm into an electrical signal and this can be done in a surprising number of ways. One of the first microphones was put together by Alexander Graham Bell. He had a job teaching kids with hearing impairments and that was how he met his wife Mabel, who was left profoundly deaf by scarlet fever. She was a smart cookie who could lip read in several languages.

One of the difficulties of profound deafness is that one cannot hear one's own voice and so it is hard to speak properly without that feedback. Bell thought that if it were possible to make a machine that displayed speech graphically, a deaf person would then have a form of feedback.

Bell's machine needed a microphone, but they didn't exist and so he had to start by making one. In fact the word microphone had yet to be coined and the earliest devices were called transmitters. Bell's first transmitter had a metal needle in the center of the diaphragm that dipped into water that was mildly acidic to make it conductive. As the diaphragm moved, the resistance varied as the depth of the needle changed in the liquid.

It worked, but barely and Bell moved on to magnetics. His next idea used a fixed magnet energized by a battery-powered coil. As Fig.1 shows, the diaphragm moved a flexible piece of ferrous material that changed the reluctance of the magnetic circuit when it moved. The varying magnetic field induced a signal in the coil.

Interestingly, when a signal was put into the coil it modified the pull of the magnet and moved the diaphragm. The device was bi-directional and when Bell connected two of them together, around 1876, the telephone was born.

Bell's microphone worked well, but it really needed an amplifier and the vacuum tube had yet to be invented. Edison and Berliner were both working on microphones, and they independently came up with a microphone that produced a higher output. The liquid of Bell's first idea was replaced with granules of carbon that the diaphragm pressed on. The variations in pressure caused different numbers of granules to be in contact and the resistance varied.

The carbon microphone made the telephone into a practical reality. It was noisy because of the discrete contacts making and breaking inside the granular carbon, but it was good enough for speech.

Mabel didn't get her speech-training machine, but she did get to live in a fabulous house and got a ride in the world's fastest hydrofoil that Alex had knocked up in his den. She watched the first airplane ever to fly in Canada with the satisfaction that she had funded it.

{% asset_img fig1.png fig1 %}
Fig.1 - Bell's first magnetic microphone used variable reluctance. Bell's patent application showed the field from a battery-powered coil energizing the magnetic circuit and the vibrations of the diaphragm caused the field to vary, modulating the battery current.

Mabel's father, Gardiner Hubbard, had been the President of the National Geographic Society. On his death, Alec Bell took over the struggling society. Pushed by his daughters to make the magazine more interesting, the idea of illustrating it with photographs and making it accessible to a wide readership was born. The rest is history.

The needs of telephony and of audio are somewhat different. Telephony is concerned with the intelligibility of speech and sonic impairments are acceptable that would not be in other applications. With the invention of the vacuum tube and the ability to amplify small signals, fidelity could take precedence over efficiency for the first time.

The heavy moving mass of the variable reluctance microphone was reduced significantly by the adoption of the moving coil principle. The idea had been around for a long time, but practical examples did not emerge until the 1930s, again primarily because of the need for amplification and powerful permanent magnets. The first alnico magnets were developed at around the same time.

Fig.2 shows that the coil is attached to the edge of the diaphragm and it moves in a constant magnetic field to generate an output. The coil should faithfully follow the vibrations of the diaphragm, yet this is a mechanical impossibility, requiring a material of infinite rigidity.

The moving coil microphone became very popular for live events because the mass of the magnet could be used to absorb handling noise. The magnet and diaphragm assembly are mounted resiliently inside an outer shell. Such microphones can also be very robust and resistant to moisture; an important matter in live events where they must be held close to limit feedback.

{% asset_img fig2.png fig2 %}
Fig.2 - The moving coil microphone has endured because of its robustness.

The ribbon microphone is also an electromagnetic transducer, but the diaphragm is conductive and when it moves in the magnetic field the output is taken from the ends of the ribbon. It can be seen in Fig.3 that there is only half a turn of a conductor in the magnet. The output is low, but so is the impedance and a useful signal can be obtained using a transformer or a low-noise amplifier.

Traditionally the ribbon microphone was heavy on account of the large magnets needed. The development of rare earth magnets of almost fantastic power yet low weight has led to a new generation of ribbon microphones.

The ribbon microphone is capable of great accuracy because the mechanical transmission of vibrations from the diaphragm to the coil is absent. The diaphragm is sensitive to wind, which generally precludes outdoor working, although modern ribbon materials have improved matters.

The discovery of piezo-electric, literally pressure-electric, materials, led to the use of the idea in microphones. Whist the name relates to pressure, in fact it is stress that causes the voltage to be developed. Piezo-electricity is bi-directional, and can be used to generate sound as well. Most wristwatches having an alarm function employ a piezo-electric element to shake the case.

The piezo-electric, or crystal, microphone used a diaphragm that was arranged to bend a bimorph, which Fig.4 shows is a strip made from two layers of material of opposite polarity. When bent, one layer would contract and the other would extend so the same signal would come out of each layer. The first crystal microphones, using Rochelle salt as the transducer, emerged in the 1930s. Crystal microphones have high output impedance and are not especially linear, but they were inexpensive and popular until better alternatives came along.

{% asset_img fig3.png fig3 %}
Fig.3 - In the ribbon microphone the diaphragm is the conductor, so the results can be very precise.

Piezo-electric sensing is today used in MEMS (micro electro-mechanical systems) because very small transducers can be made by lithography and microphone arrays can be made in very small spaces.

In contrast to what might be called electro-dynamic microphones, it is also possible to use electrostatics. If the moving coil microphone is the inverse of the traditional loudspeaker, the capacitor, or condenser, microphone is the inverse of the electrostatic speaker.

The simplest capacitor imaginable is a pair of parallel plates. In the kind of capacitor used in electronic circuits the plate spacing and the capacity are constant. However, as the capacitance changes proportionally with spacing, if one of the plates is replaced with a conductive diaphragm sound will cause the capacitance to change. If the charge on the capacitor is held constant, by charging it through an extremely high resistance, the change in capacitance translates to a change in voltage.

The condenser microphone is complicated, because it needs a power source, and the power must drive an inverter or voltage multiplier to polarize the capsule. The output signal is small and has high source impedance, so the microphone must also contain an amplifier. The first condenser microphones used vacuum tube amplifiers and were quite large and expensive, but they displayed remarkable linearity.

{% asset_img fig4.png fig4 %}
Fig.4 - The crystal microphone relies on bending a piezo-electric bimorph, which generates the output signal.

Later the electronics in the microphone were built using semiconductors that needed much less power. In the 1960s phantom powering emerged, in which the power for the microphone was fed up the same cable as carried to audio signal.

The high impedance of the condenser capsule means that it is sensitive to moisture and is not ideal as a vocal microphone for live performances. It works well in the studio for vocals where greater distance can, and indeed should, be used.

The need for a polarizing voltage in the condenser microphone was eliminated with the development of the electret. The name is to electricity what magnet is to magnetism. An electret is a material that is permanently electrically polarized and has an external electric field.

The electret microphone has the advantage that electret materials are significantly lighter than magnetic materials and the construction of very small and light microphones is possible. The microphone needs to be active, but the amount of power needed is very small and the requirement is often met by incorporating a tiny battery inside the microphone.
