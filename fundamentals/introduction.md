# Introduction and classification

## What is Jet Propulsion?

Jet propulsion is a method of generating thrust by expelling mass in one direction (a "jet"), 
which produces a reaction force in the opposite direction. 
This fundamental principle underlies all rocket and jet engines, 
from the simple water rocket to the powerful engines that launch spacecraft into orbit.

### Thrust and Newton's Third Law

**Thrust** is the force created due to a change in momentum by ejecting mass from a system. 
The principle governing thrust is Newton's Third Law of Motion: 
*every action has an equal and opposite reaction.*
When a propulsion system expels mass (such as hot gases), 
it experiences an opposite force that propels the vehicle forward.

:::{iframe} https://www.youtube.com/embed/dCF--YOjiOw?si=m3P3ab284bY_0Gpu
:width: 100%
:title: STEMonstrations: Newton's Third Law of Motion

NASA astronauts demonstrating Newton's Third Law on the International Space Station.
Skip to 1:54 to see the demo!
:::

Mathematically, thrust can be understood through the conservation of momentum. As mass is expelled at high velocity, the momentum change of the ejected mass equals the momentum change of the vehicle, but in the opposite direction.
A common engineering form for rocket thrust that we'll derive later is
$$
\label{eq-thrust}
T \approx \dot{m} V_e \;,
$$
where $\dot{m}$ is the mass flow rate (kg/s) 
and $V_e$ is the exit velocity of the exhause (m/s),
giving the thrust force $T$ (N).

:::{note}
This approximate form of thrust is based on the "momentum flux" portion of thrust;
there will also be a pressure term when the nozzle exit pressure differs from the ambient pressure.
:::

:::{important} What is a *rocket*, exactly?
A rocket is a device that produces thrust by ejecting stored matter, or **propellant**.
:::

In terms of rocket design, from Equation [](#eq-thrust) we see there are 
two primary ways to increase thrust:
1. maximize the exhaust velocity, $V_e$, or
2. increase the mass flow rate $\dot{m}$.

As we will see later, for most rocket types, $V_e$ comes from a combination 
of the chemical energy stores in the propellants and the nozzle design, 
while $\dot{m}$ is mainly a function of the engine/motor size.

With this basic definition of a rocket in mind, how can we compare the 
performance of different rocket types?

### Specific Impulse

**Specific impulse (Isp)** is a fundamental performance metric for rocket engines 
that measures the efficiency of propellant use. 
It represents the impulse (change in momentum) per unit mass of propellant consumed:
$$
I_{\text{sp}} = \frac{T}{\dot{m} g_0} \;,
\label{eq-specific-impulse}
$$
where $g_0 = 9.8066 \,\text{m}/\text{s}^2$ is the acceleration due to gravity at sea level on Earth.  
Specific impulse has units of seconds and can be thought of as 
how long one kilogram of propellant can produce one newton of thrust.

:::{warning}
You will occasionally see specific impulse given in units of speed/velocity.
In this case, simply divide by $g_0$ to convert to seconds.
:::

Higher specific impulse values indicate more efficient engines 
that can produce more thrust per unit of propellant, 
allowing for greater vehicle performance or reduced propellant requirements.


## A brief history of rocket propulsion

From Hero to von Braun.

### Ancient origins: Hero of Alexandria (10–70 CE)

The earliest known demonstration of reactive thrust comes from **Hero of Alexandria**,
a Greco-Egyptian mathematician and engineer. 
Hero created the **aeolipile** (Hero engine), a steam-powered device 
that demonstrated the principle of jet propulsion.

The aeolipile operated by heating water to generate steam. 
The high-pressure steam escaped tangentially through nozzles, 
generating thrust that caused the sphere to rotate. 
While Hero's device demonstrated reactive thrust, 
there was no mathematical explanation for the phenomenon 
until Newton's laws of motion were formulated centuries later.

:::{figure}
:label: hero-aeolipile
:align: center
:class: grid grid-cols-2 items-end gap-4

![](../images/Hero_of_Alexandria.png)

![](../images/Aeolipile_illustration.png)

[Hero](https://commons.wikimedia.org/wiki/File:Hero_of_Alexandria.png) and his [aeolipile](https://commons.wikimedia.org/wiki/File:Aeolipile_illustration.png) (image sources: Wikimedia Commons, public domain).
:::


### Chinese rockets (10th–13th century CE)

The practical development of rocket propulsion began in China 
during the 10th century with the invention of **black-powder rockets** and fireworks. 
These early rockets used gunpowder as the propellant.

By the 13th century, rockets had evolved from entertainment devices to weapons of war. 
They were reportedly used in battle during the Mongol invasion of China in 1232 CE. 
These rocket weapons were later described in detail in the *Huolongjing* 
("Fire Drake" or "Fire Dragon Manual"), compiled around 1400 CE.

:::{figure}
:label: chinese-rockets
:align: center

![Oldest depiction of rocket arrows, from the Huolongjin](../images/rocket_arrows-manual.jpg)

![Chinese solder launches fire arrow](../images/rocket_arrows-demo.gif)

Image sources: [NASA](https://web.archive.org/web/20090709050909/http://history.msfc.nasa.gov/rocketry/03.html), and [Wikimedia Commons](https://en.wikipedia.org/wiki/File:Oldest_depiction_of_rocket_arrows.jpg).
:::

The technology gradually spread beyond China to Mongolia, the Middle East, India, Korea, 
and eventually reached Europe, where it would continue to evolve.



### Congreve rocket (early 19th century)

**William Congreve** (1772–1827) developed a new generation of rocket artillery for the British military.
His designs were inspired by rockets used against the British East India Company in India. 
The **Congreve rocket** came in various sizes ranging from 6 to 300 pounds and 
represented a significant advancement in rocket warfare.

These rockets were deployed extensively during the Napoleonic Wars and the War of 1812.
They were reportedly used by both Union and Confederate forces during the American Civil War.
The Congreve rocket represented the first systematic European development of military rocket technology.

:::{figure} ../images/Congreve_rockets.png
:alt: Congreve rockets
:label: Congreve-rockets
:align: center

Congreve rockets used during the Anglo-Mysore (India) Wars. Image source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Congreve_rockets_new.png).
:::

### Jules Verne and science fiction (1878)

In 1878, science fiction author **Jules Verne** published *From the Earth to the Moon*, 
which captured the public imagination about space travel. 
In the novel, Verne used a giant cannon called the **Columbiad** 
to fire a manned projectile at the Moon from Florida. 
The spacecraft carried a crew of three.

While Verne's vision was prescient in many ways—including the Florida launch location 
and a three-person crew—the technology to achieve the necessary velocities 
using a cannon did not exist and would prove impractical due to the extreme accelerations involved.

:::{figure} ../images/From_the_Earth_to_the_Moon_Jules_Verne.jpg
:alt: Cover of From the Earth to the Moon book
:align: center
:width: 300px

Cover of early English translation of *From the Earth to the Moon* by Jules Verne.
Image source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:From_the_Earth_to_the_Moon_Jules_Verne.jpg).
:::

### The Fathers of Modern Rocketry (early 20th century)

Three pioneers are credited as the "Fathers of Modern Rocketry" 
for their theoretical and practical contributions in the early 20th century:

- **Konstantin Tsiolkovsky** (Russian teacher and mathematician)
- **Dr. Robert Goddard** (American engineer and professor)
- **Hermann Oberth** (Austro-Hungarian-born German physicist and engineer)

Additionally, **Robert Esnault-Pelterie**, a French aircraft designer and spaceflight theorist, 
made important contributions to nuclear propulsion concepts and interplanetary travel theory.

#### Konstantin Tsiolkovsky (1857–1935)

Tsiolkovsky was the first to advocate for **liquid propellant rocket engines** in 1903. 
His most enduring contribution is the **rocket equation** (also called the Tsiolkovsky rocket equation),
which relates the rocket engine exhaust velocity to the change in velocity of the vehicle:
$$
\Delta V = V_e \ln \left(\frac{m_0}{m_f}\right)
$$
where:
- $\Delta V$ is the change in velocity
- $V_e$ is the exhaust velocity
- $m_0$ is the initial mass
- $m_f$ is the final mass

This equation remains fundamental to rocket propulsion analysis today, 
and we will derive it.

:::{figure}
:label: tsiolkovsky
:align: center
:class: grid grid-cols-2 items-end gap-4

![Tsiolkovsky in 1934](../images/Konstantin_Tsiolkovsky_1934.jpg)

![First space ship draft by Tsiolkovsky (1883)](../images/Chertrg_Tsiolkovsky.jpg)

Image sources: [Wikimedia](https://commons.wikimedia.org/wiki/File:Konstantin_Tsiolkovsky_in_1934_(by_N.A.Mozhaykin).jpg) [Commons](https://commons.wikimedia.org/wiki/File:Chertrg_Tsiolkovsky.jpg).
:::



#### Dr. Robert Goddard (1882–1945)

Dr. Goddard made crucial practical contributions to rocket technology:

- **1914**: Filed patents for rocket nozzles, liquid propellant feed systems, and multi-stage rockets
- **1926**: Successfully launched the first modern rocket using gasoline and liquid oxygen, establishing the foundation for modern rocket technology
- Applied the **de Laval nozzle** (converging-diverging nozzle) to rockets, which remains the standard design today

Goddard's experimental work transformed rocketry from theory to practical engineering.

:::{figure}
:label: goddard
:align: center
:class: grid grid-cols-2 items-end gap-4

![Robert Goddard](../images/goddard.jpg)

![Goddard and liquid oxygen-gasoline rocket (1926)](../images//Goddard_and_Rocket.jpg)

Image sources: NASA ([public](https://commons.wikimedia.org/wiki/File:Dr._Robert_H._Goddard_-_GPN-2002-000131.jpg) [domain](https://commons.wikimedia.org/wiki/File:Goddard_and_Rocket.jpg)).
:::


#### Hermann Oberth (1894–1989)

In 1923, Oberth published *The Rocket into Planetary Space*, influenced by Jules Verne's science fiction.
He proposed using hydrogen and alcohol as fuels and 
later conducted experiments with liquid oxygen and gasoline. 
Oberth's work helped establish the theoretical foundations for space travel and 
inspired many future rocket engineers.

:::{figure} ../images/Hermann_Oberth_1950s.jpg
:label: oberth
:align: center
:width: 300px

Hermann Oberth in the 1950s. Image source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Hermann_Oberth_1950s.jpg).
:::

#### Wernher von Braun (1912–1977)

Von Braun represents both the technological advancement and the moral complexity of rocket development:

- Designed the **V-2 rocket** for Nazi Germany during World War II
- Had ambiguous and disputed involvement with the Nazi party and SS
- Oversaw and benefited from slave labor at the Peenemünde rocket factory
- Brought to the United States in *Operation Paperclip* following WWII
- Built upon Goddard's earlier rocket work
- Became the chief architect and engineer of the **Saturn V** heavy-lift launch vehicle for the Apollo moon missions
- Played a major role in NASA's development and advocated for crewed missions to Mars and STEM/space education outreach

:::{figure}
:label: vonbraun
:align: center
:class: grid grid-cols-2 items-end gap-4

![NASA Deputy Administrator Robert Seamans, Dr. Wernher von Braun, and President John F. Kennedy at Cape Canaveral (1963)](../images/Seamans,_von_Braun_and_President_Kennedy_at_Cape_Canaveral.jpg)

![V2 rocket](../images/V-2_rocket_diagram.svg)

Image sources: [NASA](https://commons.wikimedia.org/wiki/File:Seamans,_von_Braun_and_President_Kennedy_at_Cape_Canaveral_-_GPN-2000-001843.jpg) and Wikimedia [commons](https://commons.wikimedia.org/wiki/File:V-2_rocket_diagram_(with_English_labels).svg).
:::


## Categorization of propulsion systems

### Air-breathing vs. rocket propulsion

Propulsion systems can be fundamentally divided into two categories based on whether they carry their oxidizer or not:

#### Rocket propulsion

- **All propellants carried onboard** (both fuel and oxidizer, or single monopropellant)
- Propellants are ejected to produce thrust
- Can operate both in and out of the atmosphere (including in vacuum)
- Thrust and exhaust velocity are independent of flight speed
- Examples: liquid rocket engines, solid rocket motors

:::{figure} ../images/SolidRocketMotor.svg
:label: solid-rocket-diagram
:align: center

Diagram of solid rocket motor.
Credit: [Pbroks13 (Wikimedia Commons)](https://commons.wikimedia.org/wiki/File:SolidRocketMotor.svg).
:::

:::{figure} ../images/liquid-rocket.gif
:label: liquid-rocket-diagram
:align: center

Diagram of liquid rocket engine. Source: [NASA](https://www.grc.nasa.gov/www/k-12/airplane/lrockth.html).
:::

#### Air-breathing propulsion

- **Only carries fuel onboard**; obtains oxidizer from atmospheric air
- The majority of thrust comes from acceleration of air, combined with high mass flow rate
- The air is "free" from the atmosphere, reducing the mass that must be carried
- Exhaust velocity and flight speed are connected
- Cannot operate outside the atmosphere
- Examples: turbojets, turbofans, ramjets

:::{figure} ../images/Turbofan_operation.svg
:label: turbofan-diagram
:align: center

Schematic diagram illustrating operation of two spool, high-bypass turbofan engine.
Credit: [K. Aainsqatsi (Wikimedia Commons)](https://commons.wikimedia.org/wiki/File:Turbofan_operation.svg).
:::

### Advantages and disadvantages

**Air-breathing propulsion:**
- ✓ Advantages: Much higher fuel efficiency for atmospheric flight and higher specific impulse; reduced propellant mass
- ✗ Disadvantages: Cannot operate in vacuum; performance depends on atmospheric conditions (thrust drops with increasing altitude); limited to lower speeds (except for ramjets/scramjets)

**Rocket propulsion:**
- ✓ Advantages: Can operate anywhere (atmosphere or vacuum); performance independent of flight speed; can achieve very high velocities
- ✗ Disadvantages: Must carry both fuel and oxidizer, resulting in lower mass efficiency and lower specific impulse; requires large propellant tanks

## Types of rocket propulsion

Rocket propulsion systems can be categorized into four main types:
1. **Chemical** (liquid, solid, hybrid)
2. **Cold gas**
3. **Nuclear** (thermal, electric)
4. **Electric** (electrothermal, electrostatic/ion)

### Chemical rocket propulsion

Chemical rockets use **chemical reactions** in one or more propellants 
to produce high temperatures in the thrust/combustion chamber. 
A **converging-diverging nozzle** then converts the thermal energy (i.e., enthalpy)
into high kinetic energy, which is exhausted to produce thrust.

Chemical rockets are subdivided into three main categories:

#### Liquid propellant engines

Liquid rocket engines store propellants as liquids in tanks and 
feed them into a combustion/thrust chamber where chemical energy is released. 
The hot gases produced in the thrust chamber are then accelerated through a supersonic nozzle.

**Bipropellant systems** use separate fuel and oxidizer 
(e.g., liquid oxygen (LOX) and kerosene, or LOX and liquid hydrogen). 
The two propellants are injected into the combustion chamber where they react.

**Monopropellant systems** use a single liquid propellant 
that decomposes into hot gases when passed over a catalyst. 
Hydrazine is a common monopropellant.


Advantages:
- Thrust can be controlled and throttled
- Can be shut down and restarted
- High specific impulse (300–460 seconds for bipropellants)
- Suitable for large launch vehicles

Disadvantages:
- Complex feed systems with pumps and valves
- Requires propellant handling and storage systems, particularly challenging for cryogenics
- More expensive and complex than solid motors

#### Solid rocket motors

Solid rocket motors combine propellant storage, feed system, and thrust chamber into a **single case**. The fuel and oxidizer are mixed together into a **solid grain** that is cast or molded into the motor case.

Once ignited, the highly reactive mixture burns until the propellant is completely exhausted. The burn rate and thrust profile are determined by the grain geometry and propellant composition.

:::{figure} ../images/solid-motor-schematic.jpg
:label: solid-rocket-cutaway
:align: center

Cutaway schematic of solid rocket motor. Source: NASA (public domain).
:::

Advantages:
- Simple design with few moving parts
- High reliability
- Long storage life
- Immediate readiness (no fueling required)
- High thrust for launch applications

Disadvantages:
- Cannot be throttled or shut down once ignited
- Lower specific impulse (150–350 seconds) compared to liquid bipropellants
- Structural integrity concerns with large grain castings
- Safety concerns with large quantities of propellant


#### Hybrid propellant systems

Hybrid rocket systems combine the best features of liquid and solid rockets.
The typical configuration uses a **solid fuel grain** stored in the thrust chamber, 
with a **feed system that supplies liquid or gaseous oxidizer**. 
The oxidizer flows over the solid fuel, causing it to gasify and react, producing hot gases.

:::{figure} ../images/Hybrid_diagram.svg
:label: hybrid-diagram
:align: center

Diagram of hybrid rocket. 
Source: [Wikimedia Commons](https://en.wikipedia.org/wiki/File:Hybrids_big-tosvg.svg).
:::

Advantages:
- Safer than solid or liquid systems (oxidizer and fuel stored separately)
- Can be throttled and shut down (by controlling oxidizer flow)
- Simpler than liquid bipropellant systems
- Better performance than solid motors

Disadvantages:
- More complex than solid motors
- Fuel regression rate can be difficult to predict
- Lower performance than liquid bipropellants
- Limited flight heritage / demonstrations

### Cold gas propulsion

Cold gas systems use **stored high-pressure gas** as the working fluid. 
Common gases include air, nitrogen, and helium. 
The gas is exhausted through a nozzle to produce thrust.
These are often used for thrusters, with applications including low thrust maneuvers 
and attitude control.

:::{figure} ../images/Cold_gas_thruster_diagram.png
:label: cold-gas-diagram
:align: center
:width: 400px

Simple diagram of a cold gas thruster.
Source: [A.R. Tummala & A. Dutta; Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Cold_gas_thruster_diagram.png).
:::

Advantages:
- Very simple and reliable
- No combustion or cooling issues
- Low cost
- Ideal for low-thrust maneuvers and attitude control

Disadvantages:
- Requires heavy, high-pressure tanks
- Low performance (Isp: 60–250 seconds)
- Limited total impulse capability

**Warm gas** systems heat the gas before expansion to achieve higher performance, 
though this adds complexity.

### Nuclear propulsion

Nuclear propulsion uses nuclear reactions as the energy source rather than chemical reactions.

#### Nuclear thermal propulsion

Nuclear thermal rockets operate similarly to liquid propellant engines, 
but **nuclear fission supplies heat** to a working fluid (typically hydrogen) 
instead of chemical combustion. 
The working fluid is heated to very high temperatures by passing through a nuclear reactor core, 
then expanded through a nozzle.

:::{figure} ../images/Nuclear_thermal_rocket_en
:label: nuclear-thermal-diagram
:align: center

Diagram of a nuclear thermal rocket concept, using hydrogen as propellant.
Credit: [Tokino, vectorized by CommiM (Wikimedia Commons)](https://en.wikipedia.org/wiki/File:Nuclear_thermal_rocket_en.svg).
:::

**Performance:** Very high specific impulse (800–1,000 seconds), approximately double that of chemical rockets.

#### Nuclear electric propulsion

Nuclear electric systems use a nuclear powerplant to produce electricity, 
which then powers an electric rocket propulsion system.

:::{note} Historical context
Nuclear propulsion was extensively explored from the 1950s through the 1970s (e.g., Project NERVA), 
but concerns about nuclear safety and the political climate halted development work.
Recently, interest has grown in nuclear thermal rockets for crewed missions to Mars.
:::

Advantages:
- Very high specific impulse
- High efficiency for deep space missions
- Large total impulse capability

Disadvantages:
- High system complexity and mass
- Nuclear safety concerns
- Regulatory and political challenges
- Radiation shielding requirements

### Electric propulsion

Electric propulsion systems use **electricity to add energy to the propellant**. 
These systems offer very high specific impulse but relatively low thrust magnitude.

#### Electrothermal systems

Electrothermal thrusters (resistojets and arcjets) **heat the propellant electrically**, 
then expand it through a nozzle. Working fluids include hydrogen, ammonia, and helium.
Used for satellites since the 1970s.

#### Electrostatic/ion propulsion

Ion propulsion systems **ionize the working fluid** (typically xenon) and 
then use electric fields to accelerate the electrically charged heavy ions 
to very high velocities.

:::{figure} ../images/Electrostatic_ion_thruster-en.svg
:label: ion-thruster-diagram
:align: center

Diagram of a gridded ion thruster.
Credit: [Oona Räisänen (Wikimedia Commons)](https://commons.wikimedia.org/wiki/File:Electrostatic_ion_thruster-en.svg).
:::

Advantages:
- Very high specific impulse (500–10,000 seconds)
- Excellent for long-duration missions
- High propellant efficiency

Disadvantages:
- Very low thrust (0.0005–20 N)
- Requires significant electrical power
- Long firing times needed to achieve velocity changes
- Not suitable for launch or high-acceleration maneuvers


## Performance and typical applications

The following table summarizes the performance characteristics and 
typical applications for various propulsion technologies:

| Technology | Isp (s) | Thrust (N) | Launch | Orbit Insertion | Orbit Maintenance | Attitude Control |
|------------|---------|------------|--------|-----------------|-------------------|------------------|
| Cold gas | 60–250 | 0.5–50 | ✗ | ✗ | ✓ | ✓ |
| Solid | 150–350 | ≥13,000,000 | ✓ | ✓ | ✗ | ✗ |
| Liquid monopropellant | 200–250 | 0.5–50,000 | ✗ | ✗ | ✓ | ✓ |
| Liquid bipropellant | 300–460 | ≥6,700,000 | ✓ | ✓ | ✓ | ✗ |
| Hybrid | 300–350 | ≥13,000,000 | ✓ | ✓ | ✗ | ✗ |
| Nuclear thermal | 800–1,000 | ≥13,000,000 | * | ✓ | ✓ | ✗ |
| Electric | 500–10,000 | 0.0005–20 | ✗ | ✗ | ✓ | ✓ |

:::{note} *Note
Nuclear thermal propulsion is theoretically capable of launch 
but not currently practical due to safety and regulatory concerns.
:::

### Application insights

- **Launch vehicles** require very high thrust, typically provided by liquid bipropellant or solid rocket motors
- **Orbit insertion** requires moderate to high thrust and good efficiency, suited to liquid or solid systems
- **Orbit maintenance** (station-keeping) can use low-thrust, high-efficiency systems like electric or monopropellant
- **Attitude control** requires precise, small thrust levels, typically from cold gas or monopropellant systems

The choice of propulsion system depends on mission requirements, including required thrust level, total velocity change, mission duration, and available power.

## Key takeaways

- Thrust comes from **momentum change** by **expelling mass** (Newton's 3rd Law).
- Rockets are self-contained (carry fuel + oxidizer), enabling operation in space; 
air-breathers trade that for atmospheric intake and coupling to flight speed.
- Rocket propulsion spans a wide design space (chemical, cold gas, nuclear, electric) 
with major tradeoffs between thrust, specific impulse, complexity, and mission fit.