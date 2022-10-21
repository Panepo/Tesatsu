---
title: 'Microphones: Omnidirectional Response In Practice'
categories:
  - 手札
tags:
  - 手札
  - 轉錄
date: 2022-03-07 14:15:14
---
<br>
<center>{% asset_img title.jpg title %}</center>
<br>

{% link 原文連結 https://www.thebroadcastbridge.com/content/entry/17478/microphones-part-6-omnidirectional-response-in-practice %}

### Having looked at how microphones are supposed to work, here we see that what happens in practice isn’t quite the same because the ideal and the actual are somewhat different.

As has been stated countless times, it is the directivity of a microphone that has the greatest bearing on the results obtained. In the real world there is always sound from elsewhere along with the desired sound. Sometimes the sound from elsewhere is a nuisance to be suppressed. Sometimes it's an important aspect of the performance and it needs to be captured. Microphone directivity is about the most powerful tool in the box to approach the desired goal.

It is often stated that the omnidirectional microphone captures the greatest possible amount of ambient sound. Whilst theoretically that must be true for an ideal microphone, in practice microphones are not ideal and our conclusion might not apply to a real microphone.

All microphones require a diaphragm of finite area to extract some power from the passing sound. At low frequencies, the wavelength of the sound is so long that the microphone is vanishingly small in comparison. From a spatial sampling standpoint, we come close to Shannons's criterion that the sample should be infinitely small. From an acoustic standpoint, the presence of the microphone doesn't change anything. From an acoustic standpoint essentially it's not there. In the case of an ideal omnidirectional microphone, the physical orientation of the microphone is theoretically irrelevant.

{% asset_img fig1.png fig1 %}
Fig.1 - The finite size of a microphone diaphragm can be considered as an aperture or window. When sound arrives at an angle, a component of the window acts through time so the sound waveform is averaged or filtered.

However, this is simply not true in practice where omnidirectional microphones cannot maintain their ideal directivity at all frequencies. The shortest audible wavelengths may be of the same order as the size of the diaphragm and this changes things from both viewpoints. The spatial sampling no longer takes place at a point, but instead via a window. This is yet another example of the aperture effect that we find affecting the results in everything from loudspeakers to digital audio convertors to camera sensor chips.

The aperture effect causes a roll-off of high frequencies and is direction sensitive. The microphone no longer has the directivity we thought. Fig.1 shows that if sound approaches the diaphragm at an angle, the window causes the waveform to be time averaged, or filtered.

The controlling factor here is not the transduction technology used in the microphone, because it makes no difference how the microphone works. What matters is simply the size of the diaphragm. If the diaphragm diameter is halved, the frequency at which a particular effect is seen is doubled.

Alongside this effect, there is another one, which is that the presence of the microphone is able to change the local acoustic impedance at short wavelengths where the microphone is no longer acoustically small. This tends to cause a boost to the high frequencies received square to the diaphragm. The correct term would be on-axis, yet the ideal omnidirectional microphone isn't supposed to have an axis. Real microphones of all claimed directivities have axes.

An omnidirectional microphone can have two frequency responses. The on-axis response will show a rise at high frequencies due to the impedance change, but the manufacturer may have suppressed the effect using equalization, in which case the off-axis response may show a roll-off of high frequencies.

In all real recording spaces, the sound has a characteristic shown in Fig.2. A reverberant sound field builds up due to innumerable reflections of the sound from the source. The initial inverse-square reduction in level on moving away from the source is halted when the reverberant sound level equals the direct sound level. The distance and level at which this happens depends upon the liveliness of the space, typically measured by the reverberation time.

The difference between an architect and an acoustician is that the former spends his career trying to drive the reverberant level up whenever possible, whereas the acoustician constantly strives to bring it down.

The best way of quantifying all this is to show superimposed polar diagrams measured at a series of spot frequencies. This has been done in Fig.3 for an omni-directional microphone. At low frequencies, the ideal directivity is obtained, but as frequency rises, the effects we have noted start to cause the directivity to depart from the ideal.

{% asset_img fig2.png fig2 %}
Fig.2 - In a reverberant space, the sound level no longer falls with distance from the source when the reverberant sound level is reached.

The axis the omni microphone should not have then becomes apparent. Of all the possible directivities a microphone can have, the omni-directional microphone shows the greatest deviations from the ideal.

But what is the effect of these deviations from the ideal? Whenever directivity becomes frequency dependent, it follows that the frequency response must become direction dependent. You can't have one without the other.

Knowing how to interpret the polar plot it is possible to extract the frequency response to sound approaching from a particular direction. For example at zero degrees, or on-axis, the polar responses of Fig.3 are the same for all frequencies, telling us that the frequency response is substantially flat. However, if instead we look at an angle of 90 degrees in Fig.3, we see that low frequencies have not changed, but 10kHz is now 5dB down and 15kHz is 10dB down. The frequency response of the omni shows a strong roll-off of high frequencies at 90 degrees.

Unlike many audio situations, the problems caused by frequency dependent polar responses cannot be fixed using equalization. In the case of Fig.3, if we equalize the output of the microphone in order to make the frequency response to sound approaching at 90 degrees flat, then the sound approaching at 0 degrees will have an HF boost and sound approaching from 180 degrees will have a smaller HF loss. At 180 degrees it's even worse.

However microphones that are designed to have variable directivity often work better in omni-directional mode because they have a diaphragm at both sides of the capsule and the response at 180 degrees may be as good as the response at 0 degrees with the impaired responses at 90 and 270 degrees.

With four diaphragms mounted in a tetrahedral, the sound field microphone can be configured as an omni-directional unit that is very nearly ideal.

If the process of plotting frequency responses at different directions is repeated for a directional microphone, it will be found that the off-axis frequency response will be better than that of the omni.

{% asset_img fig3.png fig3 %}
Fig.3 - Whenever the polar diagram is not independent of frequency as is shown here, it follows that at some direction the frequency response must be impaired. Here the frequency responses at 90 degrees and 180 degrees can be seen to be anything but flat.

In a real reverberant field, such as a concert hall, where Fig.2 applies, the same relationship between direct and diffuse sound can be obtained with a microphone of any directivity, simply by placing a directional microphone a greater distance from the sound source. Theoretically the distance needs to be increased by a factor of 1.7, but that figure assumes the microphones are ideal.

The directional microphone will have a better off-axis frequency response than any omni microphone and so will reproduce the diffuse field better. That means in practice the theoretical distance factor of 1.7 times might be reduced. The oft-claimed superiority of the omni microphone for capturing ambience is a myth, whereas the inability of the omni microphone to capture directional information is a fact.

One can also conclude from consideration of the aperture effect that for the best results the microphone should have the smallest possible diaphragms consistent with other criteria being met. Small diaphragms produce smaller signals and place more stringent requirements on the noise performance of amplifiers, but electronics has made great progress in lowering noise floors and this has become less of a concern.

Not only does the small diaphragm microphone have reduced directional variation in frequency response, but it also displays less bass tip-up or proximity effect as a given amount of curvature in an approaching wave front has less effect across a smaller diaphragm.

None of this theorizing matters in the case where a microphone characteristic is deliberately being used to obtain an effect. In that case the judgment about the acceptability of the effect is entirely subjective. Paradoxically in that environment microphones may even be selected according to their defects rather than their qualities if the defects do something to the sound that is considered desirable.

As a microphone is only a loudspeaker working in reverse, we should not be surprised to find the same phenomena cropping up in loudspeakers. A typical legacy loudspeaker is omnidirectional at low frequencies and steadily becomes more directional as frequency rises. Given the greater size of loudspeakers with respect to sound wavelength, the magnitude of the problem is worse.

The result is that however good the on-axis frequency response, the off axis response will be poor. As it is the off-axis response that excites the room and the diffuse field, then the overall result will be poor. That is why it is invariably possible to tell the difference between live sound and reproduced sound emerging from the door of a room.
