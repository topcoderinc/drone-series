
# Drone Companion PC "the Agent"
Drone Series Phase 2 ran from late October 2016 through January 2017.  In addition to build a Drone Series Platform  (DSP) which allowed for consumer and providers to exchange services in a 2 sided market place we also built and REST based agent, written in NodeJS, that listened on the companion pc (raspberry pi) which was connected to the the pixhawk flight controller via serial.   The "agent" proxied instructions and locations between the drone itself and the dsp.
<img width=100% src="https://cnt-01.content-na.drive.amazonaws.com/cdproxy/templink/51yJPBLBN9QSF_yz5W9CLZQPepmoykdF3Wcg_jZOtP8eJxFPc?viewBox=4034%2C2640" />

# External Drone Tracker
The above described "agent" works great for the pixhawk,  because we have serial access to the flight controller, but we also wanted to be able to strap on a device to a ready to fly drone. To acheive this we create [droneTracker](https://github.com/kbowerma/droneTracker) which provides the same GPS smart updates to the DSP by using and particle photon](https://store.particle.io/) + [GPS](https://www.adafruit.com/product/746) + [magnometer / accelerometer](https://www.adafruit.com/products/1120)  + [Drone Tail lights -- neopixel leds and buzzer --  ](https://www.amazon.com/gp/product/B019UVHWMS).  DroneTracker updates the DSP location and in the response it can react to other drones that are too close or it can react to being in a No-Fly-Zone.  The image below shows the neopixel leds running a police siren sequence when the drone has violated a no fly zone.

<table border="0">
  <tr><td>
      <figure>
      <img width=60%  src="https://cloud.githubusercontent.com/assets/1180747/23071626/9ef6242e-f4f4-11e6-9bb4-9b453de7befc.png">
      <figcaption>3DR solo showing tail lights of droneTracker</figcaption>
      </figure>
    </td>
    <td>
      <figure>
      <img src="https://cloud.githubusercontent.com/assets/1180747/23071476/0f63c5be-f4f4-11e6-9b2b-ad20caca488d.gif" />
      <figcaption>Fig1. - A view of the pulpit rock in Norway.</figcaption>
      </figure>
  </td> </tr>
</table>

# DSP features
 * Drone provider, Drone Pilot, Consumer, and Admin Profiles
 * Ability for consumer to create a drone service request for imagery
