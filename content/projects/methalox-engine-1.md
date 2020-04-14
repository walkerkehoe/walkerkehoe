+++
content_img_path = "/images/Screen Shot 2020-04-12 at 6.20.43 PM.png"
date = 2020-03-27T07:00:00Z
layout = "project"
subtitle = ""
thumb_img_path = "/images/Screen Shot 2020-04-02 at 9.58.31 AM-1.png"
title = "Methalox Rocket Engine"

+++
### Introduction

In January of 2020 I began designing a liquid oxygen/methane rocket engine for a class at Stanford. The goal was to do a hot fire test demonstrating the engine's restart capabilities at the end of May. My team and I finalized the design and completed engineering drawings, but shortly after passing Critical Design Review (CDR) the project was cancelled due to a school-wide shutdown in response to COVID-19. See the [blog](https://walkerkehoe-6085c.netlify.com/blog/) for updates on how I've independently continued the project while quarantining. Keep reading below for a deep dive on the engine design.

### Project Goal

Hot fire test(s) demonstrating startup, shutdown and restart of a liquid oxygen/gaseous methane rocket engine.

**Stretch Goals**

* Stable combustion (defined as a chamber pressure oscillation <5% from mean)
* Measure C* efficiency
* Image engine startup and reignition

_Initially we were planning on using liquid methane but were unable to source it._

### System Parameters

<table>

<tbody> <tr> <td>Oxidizer</td> <td>Liquid Oxygen</td> </tr> </tbody>

<tbody> <tr> <td>Fuel</td> <td>Gaseous Methane</td> </tr> </tbody>

<tbody> <tr> <td>Chamber Pressure</td> <td>10 bar (\~150 psia)</td> </tr> </tbody>

<tbody> <tr> <td>Thrust</td> <td>640 N (\~144 lbf)</td> </tr> </tbody>

<tbody> <tr> <td>Throat Diameter</td> <td>25.4 mm (1 in)</td> </tr> </tbody>

<tbody> <tr> <td>O/F Ratio</td> <td>2.5</td> </tr> </tbody>

<tbody> <tr> <td>Ox Mass Flow Rate</td> <td>0.1986 kg/s</td> </tr> </tbody>

<tbody> <tr> <td>Fuel Mass Flow Rate</td> <td>0.0795 kg/s</td> </tr> </tbody>

<tbody> <tr> <td>Ox Pressurization</td> <td>Compressed Helium</td> </tr> </tbody>

<tbody> <tr> <td>Nozzle Expansion Ratio</td> <td>2.18 (sea level optimized)</td> </tr> </tbody>

<tbody> <tr> <td>Injector</td> <td>Coaxial Liquid-Centered</td> </tr> </tbody>

<tbody> <tr> <td>Igniter</td> <td>Gas-Gas Impinging Augmented Spark Igniter</td> </tr> </tbody>

<tbodyr> <tr> <td>Isp</td> <td>230 sec</td> </tr> </tbody>

</table>

Our largest design constraint was budget, which manifested itself by limiting our choice of feed line components and effectively put an upper bound on the mass flow rate we could achieve.

![](/images/Screen Shot 2020-04-12 at 5.45.39 PM.png)

We chose to run fuel rich for safety reasons and arrived at an O/F ratio of 2.5 after inputting our parameters into NASA's CEA code for a range of chamber pressures.

### P&ID Diagram

![](/images/PID-Rev09.png)

**Rationale behind the P&ID design:**

Downstream on/off valves (BVMO2, BVMF2, BVIO, SVIF2)

* Propellant feed control for run prep and start
* As close as possible to injector & igniter to minimize slosh volume

Propellant stream check valves (CKMO, CKMF, CKIO, CKIF)

* Prevent backflow into propellant tanks
* Provide closed purge volume for test abort or post-test safing

Purge check valves (CKPMO, CKPMF, CKPIO, CKPIF)

* Prevent propellant flow into purge system before & during test
* Prevent backflow in case of anomaly during purge

Flow Rate Controls (ORMO, ORMF, NVIO, NVIF)

* Mass flow rate metering via flow choking (cavitation on LOx line)
* Vernier handle needle valves for igniter mixture & flow rate tuning

Upstream on/off valves (BVMF1, SVIF1, SVIO)

* Propellant shutoff for igniter (after startup) and main injector (test termination)
* Close before downstream on/off valves to allow purge
* SVMO1 substitutes on LOx line by venting feed pressure

Pressure regulators (RGMF, RGIF, RGIO, RGN)

* Maintain steady feed pressure for gas systems to maintain steady mass flow rates through orifices

LOx System Specifics

* BVMO1: Fill control for LOx, to allow full remote control of run tank during chill-in
* SC: Load cell for LOx load monitoring
* SVMO1: LOx run tank relief & vent - could not find cryo relief valves with set pressure >1000 psi
* SVMO2: Line vent for chill-in & safing, to prevent trapped cryo volume

Helium System Specifics

* SVP: Remote control for pressurization of LOx run tank
* SVN: Remote control of propellant purge
* CKPMO: Prevent O2 backflow into inert gas system if vapor pressure rises above Nitrogen feed
* Manifold: Split purge feed to different lines

Instrumentation

* Propellant lines have P & T measurements to validate operating conditions & settings prior to test
* Cavitating venturi ORMO has PTs at inlet & throat to ensure cavitation
* Pressure downstream of metering orifices in igniter streams
  * Ensure choking (compare to regulator set pressure)
  * Monitor igniter feed conditions closely
* Igniter & main chamber pressures
  * Thrust calculation
  * Ignition check

With our components identified, we were able to run simulations to obtain a pressure ladder for the feed system. See the image below for the main injector pressure simulation.

![](/images/Screen Shot 2020-04-14 at 8.28.18 AM.png)