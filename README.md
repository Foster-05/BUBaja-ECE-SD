[![KiCad](https://img.shields.io/badge/Program-KiCad-blue?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAWCAYAAAArdgcFAAAAAXNSR0IArs4c6QAAAYBJREFUSEu1leFRAkEMhd+rQK1AOhArECtQKlAr0A6UDujAswKlAqUCsQPpgA7iPGZzEzJ7N3CD+2vvcnybfUkeNDPD/6wZjwRfA2gAbAA8ATgH0MJ/SiDe4SpdaFm5oH8zJfmhuJmNAXxH+ILkrf/YzCYAPgNsTXIU4WamTO/KuzOSynq7zEz7ucuyJCmgB18APAfYA0nBPD4H8FiLm5mSfI+Z98HfSN4HsPavFYkkmzK+KbFW8y64ajHxKxc9vwCc7NFgvXBVXeBV0fEUgPbqhLymqSFUr174yjugwJVx7iA/5Jqk4l4TzU4dntMys1zA/MkweOjbPpmHwfeQRJ/sDzezEcnfoKGKqeeuLjkIriHakJTWXqQ8tVGmg+Ga0EtvxSJPV2EHweV24+Qb6vWLVN1BcDGyqcnAdEDUfzBcB7SWWuTJ/tILz9m5s/ntd7ynHBAtN9dmZ0IX5aoOU+tFS9X7WWWK5D9abVeVZ92sOdbfXG16t97SGk7ffA+INX+jAkjEyroq/QAAAABJRU5ErkJggg==)](https://www.kicad.org/)
[![Arduino](https://img.shields.io/badge/Platform-Arduino-96D9D9?logo=arduino)](https://arduino.cc/)

# BUBaja-ECE-SD

Repository for the 2025-2026 Bucknell ECE Senior Design team working on Baja SAE.

---
<details>
<summary> <h2> Background</h2> </summary>
SAE Baja is a national competition by the Society of Automotive Engineers. It’s the sister competition of Formula Student: Baja is based off of the rally that occurs in Baja, California. Teams of students from universities across the US compete to design and manufacture the most capable off-road race vehicle they can within certain guidelines.

While this competition mainly attracts mechanical engineers, there are some electronics on the car that warrant a subsection of the team focused on ECE subjects. Electronics and controls subteams generally focus on the required electronics to run the car in accordance with the ruleset, and more fun electronics that may seem unneccesary but could help with team development or drivers during events.

<h4>Required electronics are as follows:</h4>
<details>
<summary>Killswitches</summary>
<blockquote>
B.10.3 - Engine Kill Switches

Engine kill switches shall be employed to ground the ignition circuit and shut down the engine. Cut-out or
disabling switches or devices preventing the immediate function of the engine kill switches are strictly
prohibited.

B.10.3.1 - Quantity

Each vehicle shall be equipped with a minimum of two (2) engine kill switches.

B.10.3.2 - Required Switch

The vehicle shall be equipped with one or more of the following required switches:
• Polaris Part 4015321 or 4019114
• <a href='http://www.mfgsupply.com/01-171.html'>Ski-Doo Part 01-171</a>
• <a href='http://www.parkeryamaha.com/skidoostopswitch.aspx'>WPS 27-0152</a>
• <a href='http://www.parkeryamaha.com/skidoostopswitch.aspx'>WPS 27-0154</a>

The switches listed above shall only be used as engine kill switches.
</blockquote>
We own two of these required switches already and will continue to reuse them.
<blockquote>
B.10.3.3 - Location

B.10.3.3.1 - Cockpit Switch

A minimum of one cockpit kill switch is required as defined by this rule. Additional cockpit kill switches are
permitted provided the switch meets rule B.10.3.2 - Required Switch.
The cockpit kill switch shall be mounted on the left side of the driver, along the SIM, within reach of a
driver that is properly secured in the vehicle. No other push button switches may be mounted along the
Left SIM. Restraining the driver in any way to prevent accidental contact is explicitly prohibited.

B.10.3.3.2 - External Switch

One of the required kill switches shall be located within easy access to track workers on the right side of
the vehicle, aft of the plane of the RRH, and forward of the right FABUP. The external kill switch shall be
generally perpendicular to the firewall (±15 deg), the axis of the switch action generally horizontal (±15
deg), below named point B R , and no further than 180 mm (7.0 inches), dimension “Z” in Figure B-58 ,
below named point BR , and shall be mounted on a tab connected directly to the RRH. The external kill
switch shall not be recessed more than 51 mm (2.0 inches) from the outside edge of the RRH tube.

B.10.3.4 - Mounting

All engine kill switches shall be rigidly mounted to the vehicle frame with unobstructed access to the
switch. All engine kill switches shall be free and clear of sharp edges or other hazardous conditions to
track workers or the driver. All switches shall be mechanically fastened to the frame. Adhesives are
explicitly prohibited. If any threaded fasteners are used to mount an engine kill switch, they shall meet the
requirements of Article 12 - Fasteners. Any type of guard, cover, or obstruction to prevent accidental
contact is explicitly prohibited within 3" of the kill switch.

Note: Rivets and other robust, captive methods are acceptable fasteners for fastening kill switches to the
mounting tab. Technical inspectors will evaluate each of these designs individually.
</blockquote>
</details>

<details>
<summary>Wiring Harness</summary>
The engine requires power to the spark plug, as well as wire routing to killswitches and to brake lights.
<blockquote>
B.10.2 - Wiring and Connectors

B.10.2.1 - Wire Routing

All vehicle wiring and connectors shall be cleanly and neatly installed. Wiring shall be routed away from
sources of excessive heat, abrasion, chafing, and possible short circuit. Wiring shall be installed and
routed such that it does not become a hazard to cockpit egress.

B.10.2.2 - Wire Termination

Wires shall be properly terminated with appropriate terminals and fittings for all connections. Bare wire
connections are not permitted. (i.e. bare wire under a screw terminal, wire nuts, etc)

B.10.2.3 - Connectors

Cable and wiring terminations shall have features to protect against reverse polarity connection
</blockquote>
</details>


<details>
<summary>Signaling </summary>
<blockquote>
B.10.4 - Signaling

Each vehicle shall be equipped with signaling devices. Cut-out or disabling switches or devices
preventing the immediate function of the required signaling devices are strictly prohibited.

B.10.4.1 - Brake Light

All vehicles are required to have a functional brake light to signal to other drivers the vehicle is stopping or
slowing down.

B.10.4.1.1 - Required Brake Light

Only the following brake lights are permitted. Brake lights not listed are explicitly prohibited. Modification
of the brake light from the OEM design is explicitly prohibited. All brake lights shall be configured to be
fully illuminated when the brakes are applied, and completely extinguished with the brakes are released.
• Polaris Part # 2411450
• Polaris Part # 2411099
• Polaris Part # 2411092-432
• Haul-Master – Part # 93263
• Command Electronics Part # 003-6018R
• Command Electronics Part # 003-6016

B.10.4.1.2 - Location and Orientation

The vehicle brake light shall have a resilient and durable mount and be positioned at a minimum of 1000
mm (39.4 in.) above the ground. The vehicle brake light shall be oriented to be visible to trailing vehicles
and shine parallel to the ground or at a slightly downward angle. Brake lights angled (aimed) above a
horizontal plane are not permitted. The brake light must be visible at least at a 45 degree angle from the
left and right of center, for a total field of view of at least 90 degrees.

B.10.4.1.3 - Brake Light Switch

The brake light shall be activated only by a hydraulic pressure switch installed in the brake hydraulic lines.
Each independent hydraulic brake circuit must be equipped with a hydraulic pressure switch. Cutting
brakes are required to activate the brake light by way of a hydraulic pressure switch.

B.10.4.2 - Reverse Light

Vehicles with a reverse gear shall be equipped with a reverse light. The reverse light shall illuminate
when the vehicle is shifted to reverse gear and is extinguished when the vehicle is shifted out of reverse
gear.

B.10.4.2.1 - Specification

Reverse lights shall be marked with an SAE “R” on the lens of the reverse light and be of LED design,
equal to or exceeding the SAE standard J759.

B.10.4.2.2 - Location and Orientation

The reverse light shall have a resilient and durable mount and be positioned at a minimum of 700 mm
(27.6 in.) above the ground. The reverse light shall be oriented to be visible to trailing vehicles and shine
generally parallel to the ground.

B.10.4.3 - Reverse Alarm

Vehicles with a reverse gear shall be equipped with an audible reverse alarm. The reverse alarm shall
sound when the vehicle is shifted to reverse gear and silenced when the vehicle is shifted out of reverse
gear.

B.10.4.3.1 - Specification

Required reverse alarms shall be rated to meet the SAE standard J1741 or J994.

B.10.4.3.2 - Location

Required reverse alarms shall be mounted to the vehicle frame aft of the plane of the RRH.
</blockquote>

The team does not currently have plans to implement reverse in the upcoming year's car.
</details>

<h4>"Fun" electronics can include the following:</h4>

• Digital dash

• Steering wheel with indicators

• Drive-by-wire

• Electronic differentials
<details>
<summary>Rules on additional electronics</summary>

B.10.5 - Instrumentation

Vehicles may be equipped with instrumentation to provide operational or performance information to the
driver. All vehicle instrumentation must be included in the cost report.

B.10.6 - Data Acquisition

Vehicles may be equipped with data acquisition (data logging) systems. Data acquisition systems
providing feedback to the driver must be included in the cost report. Data acquisition systems not
providing data to the driver may be excluded from the cost report.

B.10.7 - Communication Systems

Teams are permitted to use radio-frequency (RF) communications systems. Any team using RF systems
shall comply with federal, state, and local regulations based on the location of the event. At no point may
a team’s RF systems cause harmful interference to the voice or data systems in service of competition
officials or emergency responders.

B.10.7.1 - Voice

Vehicles are permitted to use RF voice communications systems. RF Voice communication systems and
equipment may be excluded from the cost report.

B.10.7.2 - Data

Vehicles are permitted to use RF data communications systems. All RF data communications systems
and associated hardware may be excluded from the cost report. Exception: If a data communications
system provides feedback to the driver, it shall be included in the cost report.
</details>

And many more!

Teams may choose what they prefer to explore and spend their time on. Our current priorities lie in having an entirely functional car, especially with our electronic differentials and some data output for the driver.

</details>

<details>
<summary> <h2>Scope</h2></summary>
Bucknell's ECE Senior Design team will be focused on some of these additional
 electronics. The subteam will continue to handle the wiring harness,
 including power delivery, indication, and killswitches. The senior design team has several
options, including but not limited to some of the fun electronics listed in the
Background section. They may elect to pursue whatever project they deem most valuable
to the team within their budget and time constraints, but the club would prefer a 
focus on the electronic differentials and/or data acquisition, two things that would
significantly improve the performance of the car if they work reliably and consistently.

</details>

<details>
<summary><h2>Contact Information</h2></summary>
The electronics team can be reached through Tyler Seitz, Eli Foster or Aiden Cherniske. Contact through Discord or Bucknell email.
Matt Raudabagh is the president of the Bison Racing club and oversees higher-level coordination of teams.
Craig Beal is the advisor for both Mechanical Engineering Senior Design and the Bison Racing club. He can be contacted as a tertiary source.
</details>

Here are some resources that should help:

<a href='https://eg.bucknell.edu/~baja/doku.php?id=main'>Bucknell-hosted Baja Wiki</a>

<a href=https://www.bajasae.net/cdsweb/gen/DocumentResources.aspx>Baja documentation</a>

<a href=https://github.com/ACherniske/E-C-Subteam-Bucknell-Baja>Previous subteam repository</a>

<a href=https://discord.gg/9MWbHbAc>National Baja SAE Discord</a>

