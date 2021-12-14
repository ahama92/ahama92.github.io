---
bibliography:
- 'document.bib'
title: Stability Analysis of Oblique Wing Airplanes
---

![image](root/ubc.png){width="20%"} \

------------------------------------------------------------------------

------------------------------------------------------------------------

[**Author**]{.smallcaps}\

Mohammad Zandsalimy\

Abstract {#abstract .unnumbered}
========

Oblique wing airplanes were investigated for a long time with the
promise of combining efficient subsonic as well as supersonic flight
characteristics. The first known oblique wing design was the Blohm &
Voss P.202, proposed by Richard Vogt in 1942. Further, NASA AD-1
(Ames-Dryden-1) aircraft utilized a wing that could be pivoted obliquely
from zero to 60 degrees during flight. The aircraft was flown 79 times
during the research program, which evaluated the basic pivot-wing
concept and gathered information on handling qualities and aerodynamics
at various speeds and degrees of pivot. Further, there has been several
test flights to prove the feasibility and performance of oblique wings.
NASA Ames also developed an oblique wing airplane from their F-8
digital-fly-by-wire airplane. This design can produce higher lift to
drag ratios over a wide range of flying speeds. Such airplanes, however,
show large cross-coupling in their control and dynamic behavior which is
not present in conventional symmetrical airplanes. Such behavior must be
compensated to obtain acceptable handling qualities. Furthermore, R.T.
Jones of NASA Ames Research Center has conducted some of the earliest
theoretical studies on this subject, beginning in the 1950s. In the
present project, first, I will give a historical review of oblique wing
airplanes and other oblique wing studies and summarize the results. I
will then use XFLR5 software to analyze the characteristics and
performance of NASA AD-1 wing (at zero sweep). I will also utilize
lifting line theory to analyze the effect of oblique angle on the
induced drag. At low speeds, the most efficient lifting surface is a
high aspect ratio elliptically loaded wing because drag due to lift is
inversely proportional to the aspect ratio. At transonic and supersonic
speeds, however, wave drag is the dominant part of the total drag. A
significant advantage of oblique wing arrangements for supersonic flight
is that they distribute the lift over about twice the wing length
compared to a conventional, symmetrically swept wing. This reduces lift
dependent wave drag by a factor of 4 and volume dependent wave drag by a
factor of 16.

Keywords: Oblique Wing, Aerodynamic Performance, Airplane Stability.

Introduction
============

No doubt, straight wing airplanes are most efficient in low speed
flight, but swept wings are essential in an aircraft designed for
transonic or supersonic flight. Supersonic flight missions usually have
high swept (or even delta) wings. Unfortunately, the stall speed
increases with increasing sweep which means longer takeoff distance
requirement. Further, high sweep can increase the parasite drag in
subsonic flights which increases the fuel consumption in this phase. A
variable sweep wing allows the use of optimum sweep angle for the
aircraft's current phase of flight (related to flight speed). A number
of experimental designs were carried out prior to the 1970s and a few
variable sweep airplanes (including Grumman F-14 Tomcat) are still in
use. Figure
[\[fig\_f14\_tomcat\_1\]](#fig_f14_tomcat_1){reference-type="ref"
reference="fig_f14_tomcat_1"} shows the Grumman F-14 Tomcat aircraft
testing an unusual asymmetric wing configuration with one wing at
minimum sweep and the other at maximum sweep. Recent advances in flight
control and structural materials allows more advancement in variable
geometry aircraft. New designs are less focused on variables sweep to
achieve the required performance. Instead, wings are given complicated
flaps on both leading and trailing edges that change the effective
camber or chord of the wing to adjust to the flight regime. Such
configurations are also a form of variable geometry wings
[@bolonkin1999estimated]. Variable geometry wings are wings that are
capable of changing their shape in some way during flight which can be
divided into the following categories:

-   Variable sweep wings known as swing wing (e.g. Sukhoi Su-24).

-   Variable incidence wings with an adjustable angle of incidence
    relative to its fuselage (e.g. RF-8A Crusader).

-   Variable camber (and/or chord) wings in which the leading and/or
    trailing edge sections of the whole wing pivot to increase the
    effective camber, modifying the maximum lift coefficient.

-   Oblique wings also known as slewed wings which are designed in a way
    to rotate about the center point, so that one tip is swept forward
    while the opposite tip is swept aft.

![A Grumman F-14 Tomcat during a test of an unusual asymmetric wing
configuration (courtesy of San Diego Air & Space Museum
Archives).](Grumman_F-14_Tomcat_SDASM.jpg){width="55%"}

[\[fig\_f14\_tomcat\_1\]]{#fig_f14_tomcat_1 label="fig_f14_tomcat_1"}

As the 1940s came to a close, military aircraft manufacturers in the
United States faced a disturbing problem. The Bell X-1 had broken the
sound barrier, and both the Air Force and the Navy were looking for next
generation aircraft that could operate at supersonic speeds. But
preliminary tests of models indicated that even the best designs put
forth by industry engineers were not going to be able to achieve that
goal. A sharp increase in drag at speeds approaching mach number one was
proving too much for the limited power of jet engines in that time to
overcome. The solution to this frustrating impasse was found by Richard
T Whitcomb, a young aerodynamic scientist at NACA Langley Research
Center in Hampton, Virginia. His development of the \"area rule\"
revolutionized how engineers looked at high-speed drag and impacted the
design of virtually every transonic and supersonic aircraft ever built.
In recognition of its far-reaching impact, Whitcomb's area rule was
awarded the 1954 Collier Trophy [@hansen1987engineer].

The Whitcomb area rule is a design technique used to reduce an
aircraft's drag at transonic and supersonic speeds. Transonic
acceleration is considered an important performance metric for airplanes
and which is directly dependent upon wave drag. This rule states that
small changes in cross sectional area of the aircraft will prevent high
wave drag at transonic flight regimes. Straight wings are a large change
in the cross sectional area of the airplane. Swept wings have a more
gradual change in the cross sectional area. Further, oblique wings tend
to remedy this problem in an unusual and effective way. An oblique wing
can vary the wing sweep with a single pivot that is primarily loaded in
tension, trading aspect ratio for fineness ratio[^1] by sweeping one
wing tip forward and the other wing tip back. This design allows a
greater reduction in the wave drag, automatically accounts for area
ruling, and reduces pivot torque and bending loads as well as fuselage
loads. As presented in figure
[\[fig\_oblique\_vs\_symmetric\_2\]](#fig_oblique_vs_symmetric_2){reference-type="ref"
reference="fig_oblique_vs_symmetric_2"}, the torque and bending loads
from wing pivots can be avoided utilizing an oblique wing.

![Comparison of load and moment distribution for oblique and
symmetrically swept wings (courtesy of NASA Langley Research
Center).](oblique_wing_loads_1.jpg){width="75%"}

[\[fig\_oblique\_vs\_symmetric\_2\]]{#fig_oblique_vs_symmetric_2
label="fig_oblique_vs_symmetric_2"}

Oblique wing airplanes can be utilized for both military and civilian
missions. Main advantages of such airplanes is for airplanes with
subsonic as well as supersonic regimes in their flight envelope. Oblique
wing configuration will have lower wave drag, less structural weight,
and reduced hangar parking and storage area compared to other variable
geometry aircraft. Many analytical studies, wind tunnel tests, and low
speed light weight flights have been conducted on such airplanes, but no
high performance aircraft has been developed due to high risks
associated with such revolutionary designs [@gregory1985oblique]. The
advantages of oblique wings cannot be obtained without overcoming many
design challenges. Dynamic behavior and response of such wing
configuration is not even close to the conventional symmetric airplanes.
The flight control system has to provide lateral-directional (roll-yaw)
decoupling so that good stability and handling are provided for the
pilot during the flight envelope.

One of the most notable scientists to work on the development and
advancement of oblique wings is American aerodynamicist and aeronautical
engineer, Robert Thomas Jones. Between 1946 and 1958, Robert T. Jones
conducted various studies on swept and delta-wing aerodynamics, making
notable contributions to understanding the relationship between planform
choice and aerodynamic performance. Jones was firmly committed to the
study of bilaterally symmetric swept-wing shapes. But in 1952, he
deviated from the bilaterally symmetric path to address the case of the
elliptical wing. The elliptical wing is one of the oldest and most
pleasing aerodynamic shapes. Earlier in his career, Jones had studied
the conventional elliptical wing, and now, in the early supersonic era,
he returned to study it, finding that an elliptical wing set at an
oblique angle not only had a highly desirable uniform lift distribution,
but a greatly reduced drag as well [@robert1952theoretical]. Figure
[\[fig\_rtjones\_1\]](#fig_rtjones_1){reference-type="ref"
reference="fig_rtjones_1"} shows a photo of R.T. Jones working on a
violin. Also in this photo, notice the oblique wing radio controlled
model airplane and a reflector telescope, also made by Jones.

![Robert T. Jones making a violin (courtesy of Roger Ressmeyer from
Corbis Images).](rtjones_1.jpg){width="75%"}

[\[fig\_rtjones\_1\]]{#fig_rtjones_1 label="fig_rtjones_1"}

I am sure model aircraft have a long and distinguished history of
contributing to the development of aeronautics. Jones made a balsa wood
model of an oblique wing airplane which he flew at the first
International Congress of the Aeronautical Sciences (ICAS), held in
Madrid, Spain, in September 1958. A great deal of work has been done
since on oblique wing aircraft including design work by Boeing, General
Dynamics, and Lockheed, wind tunnel testing and analysis by NASA, and
flight testing of models and piloted aircraft. Figure
[\[fig\_AD\_1\]](#fig_AD_1){reference-type="ref" reference="fig_AD_1"}
shows the AD-1 oblique wing research aircraft in flight.

![The AD-1 oblique wing research aircraft (courtesy of NASA Photo ECN
13305-4).](AD-1.jpg){width="85%"}

[\[fig\_AD\_1\]]{#fig_AD_1 label="fig_AD_1"}

The general idea is to design an aircraft that performs with high
efficiency as the Mach number changes during flight envelope. Since
different types of drag dominate in each flight regime, uniting high
performance designs for each regime into a single airframe can be
challenging. Induced drag is the dominant part in low Mach number
flight, while wave drag becomes important at high Mach numbers. One way
to reduce induced drag is to increase the effective wingspan of the
lifting surface as seen in most gliders. One important thing about
gliders is their low take off weight which suggests very low lift
generation which in turn means that structural concerns are very
important in glider construction. An ideal wing has infinite span
without induced drag. At lower air speeds, an oblique wing is positioned
perpendicular to the fuselage (just like a conventional wing) to provide
maximum lift and control qualities. As the flight speed increases, the
wing is pivoted to increase the oblique angle which reduces drag and
fuel consumption.

Further, at higher Mach numbers, wave drag is dominant. Sweeping the
wings away from the nose (where shock waves happen) can keep the wings
downstream of the wave which greatly reduces drag. By actively
increasing sweep as Mach number increases, high efficiency is possible
for a wide range of air speeds. Although one of the principal advantages
involves reduced supersonic wave drag, the concept has other merits as
well.

There are three main components of wave drag as follows:

-   Volume distribution (i.e. area rule)
    $$D \sim \dfrac{\text{Volume}^2}{\text{Length}^4}$$

-   Lift distribution $$D \sim \dfrac{\text{Lift}^2}{\text{Length}^2}$$

-   Sweep effect (at root) $$D \sim \cos(\Lambda)$$

Figure
[\[fig\_oblique\_vs\_swept\_1\]](#fig_oblique_vs_swept_1){reference-type="ref"
reference="fig_oblique_vs_swept_1"} compares the length of an oblique
wing and a symmetrically swept wing with the same sweep angle. Length of
the oblique wing is almost twice as much as the symmetric swept wing.
This means that the wave drag component due to volume distribution is
about $\frac{1}{16}$ and the component due to lift distribution is about
$\frac{1}{4}$ when comparing the oblique to swept wing. Furthermore,
when compared to an aircraft with symmetric variable sweep, the oblique
wing has little change in the aerodynamic center position. This keeps
the stability at reasonable levels and avoids large trim changes or
complex fuel-pumping schemes.

![Comparison of length of oblique and symmetrically swept wings
(courtesy of Could not Find the
Source).](oblique_vs_sweep_1.jpg){width="45%"}

[\[fig\_oblique\_vs\_swept\_1\]]{#fig_oblique_vs_swept_1
label="fig_oblique_vs_swept_1"}

Figure
[\[fig\_drag\_comparison\_1\]](#fig_drag_comparison_1){reference-type="ref"
reference="fig_drag_comparison_1"} shows a comparison between various
drag components of the configurations presented in figure
[\[fig\_various\_configurations\_1\]](#fig_various_configurations_1){reference-type="ref"
reference="fig_various_configurations_1"} for flight at a Mach number of
0.9. As seen here, the oblique wing at 50$^o$ has less total drag than
all configurations, with even less wave drag than the delta wing. The
viscous drag of the oblique wing is less than the delta wing due to less
area. Further, the worst performing wing is the simple configuration
without any sweep which sports almost twice as much drag as the oblique
wing at 50 degrees. The wave drag has been reduced in all the swept wing
planforms but the oblique wing with 30$^o$ sweep has 8.95% less total
drag compared to sweptback wing of 30$^o$ sweep and 40.63% lower total
drag compared to 0$^o$ sweep. The oblique wing with 50$^o$ sweep has
34.8% less total drag compared to sweptback wing of 30 $^o$ sweep,
10.17% less compared to Delta wing of 65$^o$ sweep and 57.49% less
compared to 0$^o$ sweep. R. T. Jones predicted such benefits before
experimental testings. Figure
[\[fig\_prediction\_1\]](#fig_prediction_1){reference-type="ref"
reference="fig_prediction_1"} shows his prediction of drag coefficients
vs. Mach number for a symmetrically swept wing and an oblique wing at
50$^o$.

![Five different configurations of wings flying at Mach = 0.9
[@alam2014oblique].](configurations_Mach09.jpg){width="95%"}

[\[fig\_various\_configurations\_1\]]{#fig_various_configurations_1
label="fig_various_configurations_1"}

![Comparison of drag components of different wing configurations flying
at Mach = 0.9 [@alam2014oblique].](drag_comparison.eps){width="85%"}

[\[fig\_drag\_comparison\_1\]]{#fig_drag_comparison_1
label="fig_drag_comparison_1"}

![Prediction of drag coefficient vs. Mach number
[@jones1973dual].](rtprediction.jpg){width="55%"}

[\[fig\_prediction\_1\]]{#fig_prediction_1 label="fig_prediction_1"}

The concept of an oblique all wing aircraft was first proposed by Lee
[@lee1961slewed] in the early 1960's, but subsequent research on oblique
wing aircraft up to the mid 1980's concerned oblique wing/body aircraft
with the oblique wing pivoted from a conventional fuselage. The 3-view
sketch of figure
[\[fig\_all\_oblique\_1\]](#fig_all_oblique_1){reference-type="ref"
reference="fig_all_oblique_1"} shows the concept proposed by Lee.
Despite several questions about stability and control, this concept can
be made to fly. The model shown in figure
[\[fig\_all\_oblique\_model\_1\]](#fig_all_oblique_model_1){reference-type="ref"
reference="fig_all_oblique_model_1"} weighed about 80 lb (36 kg) with a
20 ft (6 m) wing span and was powered by two ducted fan engines. The
aircraft is unstable and controlled actively with a custom built flight
control computer. The project was undertaken at Stanford University in
1991-1994, principally by Steve Morris and Ben Tigner
[@morris1995flight].

![Oblique all wing concept proposed by G. H. Lee
[@lee1961slewed].](all_oblique_1.jpg){width="55%"}

[\[fig\_all\_oblique\_1\]]{#fig_all_oblique_1 label="fig_all_oblique_1"}

![An oblique all wing aircraft model
[@morris1995flight].](stanford_oblique.jpg){width="75%"}

[\[fig\_all\_oblique\_model\_1\]]{#fig_all_oblique_model_1
label="fig_all_oblique_model_1"}

One of R. T. Jones explanations on the reduced wave drag was about
pressure signals (Mach lines) and shock waves. Elementary pressure
signals propagate at the speed of sound relative to a fluid. In a
subsonic oncoming stream, the disturbance from an unswept wing (or any
obstacle for that matte) propagates upstream against the flow and causes
the streamlines to begin to curve to avoid the obstacle, thus keeping
the drag to a desirably low value. In a supersonic flight, by contrast,
signals are confined to a shock wave originating at a point of
disturbance. Jones considers an infinitely long wing immersed in a
supersonic flow of speed V and swept at different angles in relation to
a Mach line. For angles of sweep $\beta$ less than that of the Mach line
(Figure
[\[fig\_rtjones\_machline\_1\]](#fig_rtjones_machline_1){reference-type="ref"
reference="fig_rtjones_machline_1"}a), the leading edge cannot affect
the approaching flow, which thus impacts the airfoil undisturbed,
resulting in a large drag. For angles of sweep greater than that of the
Mach line (Figure
[\[fig\_rtjones\_machline\_1\]](#fig_rtjones_machline_1){reference-type="ref"
reference="fig_rtjones_machline_1"}b), the wing experiences a subsonic
flow. As a result, the streamlines will curve around and follow paths
appropriate to a subsonic flow and the drag can be expected to be
correspondingly low [@Walter2005].

![Mach line in two different angles of sweep
[@jones1946wing].](rtjones_mach.jpg){width="35%"}

[\[fig\_rtjones\_machline\_1\]]{#fig_rtjones_machline_1
label="fig_rtjones_machline_1"}

AD-1 Aircraft
=============

The AD-1 airplane consists of a high fineness ratio fuselage with two
French Microturbo TRS-18 engines, each with a sea level thrust rating of
220 pounds. The engines are mounted on short aft pylons on the side of
the fuselage and consume 72 gallons of jet fuel stored in two fuselage
tanks installed fore and aft of the wing pivot. The AD-1 has
conventional horizontal and vertical tails, fixed gear, and a high
aspect ratio ($\AR = 11.3$ zero sweep) oblique wing. The wing can be
pivoted in flight from a 0 degree to 60 degree sweep (with the right
wing forward) on a pivot point at the 40% of root chord location. The
center of gravity while in flight was generally within a few percent of
the nominal quarter root chord position. Table
[\[table\_ad\_1\_summary\]](#table_ad_1_summary){reference-type="ref"
reference="table_ad_1_summary"} summarizes the general and performance
characteristics of AD-1 aircraft. Figure
[\[fig\_AD\_1\_photo\_1\]](#fig_AD_1_photo_1){reference-type="ref"
reference="fig_AD_1_photo_1"} shows the overhead view of this aircraft
in a flight with non zero oblique angle. Figure
[\[fig\_AD\_1\_photo\_2\]](#fig_AD_1_photo_2){reference-type="ref"
reference="fig_AD_1_photo_2"} shows three view sketch of AD-1 aircraft.
Using this photo and the specifications provided in table
[\[table\_ad\_1\_summary\]](#table_ad_1_summary){reference-type="ref"
reference="table_ad_1_summary"}, the wing geometry is extracted to be
used latter on. This wing model has zero angle of incidence and
dihedral. This geometry is presented in table
[\[table\_geom\_1\]](#table_geom_1){reference-type="ref"
reference="table_geom_1"}. Another important note is that this aircraft
does not utilize flaps.

[\[table\_ad\_1\_summary\]]{#table_ad_1_summary
label="table_ad_1_summary"}

  ----------------- ----------------------------------------------------------------------
  Crew              1 (pilot)
  Length            38 ft 10 in (11.83 m)
  Wingspan          32 ft 4 in (9.85 m) unswept
  Lower wingspan    16 ft 2 in (4.93 m) swept 60$^o$ sweep angle
  Height            6 ft 9 in (2.06 m)
  Wing area         93 sq ft (8.6 m$^2$)
  Airfoil           NACA 3612-02, 40
  Empty weight      1450 lb (658 kg)
  Gross weight      2145 lb (973 kg)
  Fuel capacity     80 US gallons (300 l)
  Powerplant        2$\times$ microturbo TRS 18 turbojets, 220 lbf (0.98 kN) thrust each
  Maximum speed     200 mph (320 km/h, 170 kn)
  Service ceiling   12000 ft (3700 m)
  ----------------- ----------------------------------------------------------------------

  : AD-1 aircraft characteristics.

![AD-1 aircraft at flight (courtesy of NASA Photo ECN
15846).](AD-1_ObliqueWing_60deg_19800701.jpg){width="65%"}

[\[fig\_AD\_1\_photo\_1\]]{#fig_AD_1_photo_1 label="fig_AD_1_photo_1"}

![Three view sketch of Ad-1 aircraft (courtesy of NASA Dryden AD-1
Graphics Collection).](AD1-scissorwing-3views.jpg){width="65%"}

[\[fig\_AD\_1\_photo\_2\]]{#fig_AD_1_photo_2 label="fig_AD_1_photo_2"}

[\[table\_geom\_1\]]{#table_geom_1 label="table_geom_1"}

     y     chord   offset
  ------- ------- --------
     0     1.338     0
   0.965   1.185   0.071
    2.7    0.87    0.224
   3.578   0.717    0.28
   3.991   0.621   0.315
   4.357   0.544   0.341
   4.775   0.382   0.392
   4.925     0     0.575

  : AD-1 wing geometry.

Structurally, the airplane consists of a fiberglass reinforced plastic
sandwich with a core of rigid foam. The thickness varies from 17 plies
at the wing root to 4 plies at the tip. Except for the wing pivot, all
other components were designed to a 6 g load limit capacity. The wing
pivot was designed to withstand $\pm$25.0 g loading. The airplane weighs
approximately 2100 pounds and has potential performance speeds up to 175
knots and flight at altitudes of up to 15000 feet. The above
specifications were considered conservative since the aircraft was not
expected to exceed 5 g loading or 150 knot speed in order to accomplish
the program's research goals [@larrimer2013thinking].

XFLR5 Analysis
==============

In this section, the wing of AD-1 aircraft is imported into XFLR5
software and analyzed in different conditions. Unfortunately, XFLR5 is
not able to analyze oblique wings. As a result, this study will be
carried out for the wing at zero degrees of oblique angle. First test is
done at a constant speed of 80 m/s and at a cruise height of 3000 m. In
this conditions, tip Reynolds number is about 2 million, while root
Reynolds number is about 7 million. Figure
[\[fig\_1\_clvsalpha\]](#fig_1_clvsalpha){reference-type="ref"
reference="fig_1_clvsalpha"} shows the plot of lift coefficient vs.
angle of attack. The lift coefficient slope is about 0.092726 per degree
and stall occurs at 21 degrees. Zero lift angle is -1.5546 degrees.
Different components of drag and total drag are plotted vs. angle of
attack in figure
[\[fig\_1\_cdvsalpha\]](#fig_1_cdvsalpha){reference-type="ref"
reference="fig_1_cdvsalpha"}. At high angles of attack (near stall) the
rate of increment in induced drag reduces slightly and the rate of
increment in parasite drag increases. Further, figure
[\[fig\_1\_clvscd\]](#fig_1_clvscd){reference-type="ref"
reference="fig_1_clvscd"} shows the drag polar of this wing. The minimum
drag coefficient happens at -0.5 degrees angle of attack which
corresponds to a drag coefficient of 0.004618 and a lift coefficient of
0.100232. Figure
[\[fig\_1\_clovercdvsalpha\]](#fig_1_clovercdvsalpha){reference-type="ref"
reference="fig_1_clovercdvsalpha"} shows the plot of $C_L/C_D$ vs. angle
of attack. The maximum value of $C_L/C_D$ happens at $\alpha=2$ degrees
and corresponds to a value of $C_L/C_D=43.3543$. At the design angle of
attack the distribution of lift coefficient and induced angle of attack
over the span of the wing are plotted in figures
[\[fig\_1\_clvsy\]](#fig_1_clvsy){reference-type="ref"
reference="fig_1_clvsy"} and
[\[fig\_1\_aivsy\]](#fig_1_aivsy){reference-type="ref"
reference="fig_1_aivsy"}, respectively. As seen in figure
[\[fig\_1\_clvsy\]](#fig_1_clvsy){reference-type="ref"
reference="fig_1_clvsy"}, lift coefficient increases up to about 50% of
half span and the stays almost constant up to 90% and then suddenly
decreases. The same thing in reverse happens to induced angle of attack.
As seen in figure [\[fig\_1\_aivsy\]](#fig_1_aivsy){reference-type="ref"
reference="fig_1_aivsy"}, induced angle of attack decreases until about
50% of half span and the stays almost constant up to 90% and then
suddenly increases.

![Lift coefficient vs. angle of attack at $U_{\infty}=80$
m/s.](1_clvsalpha.eps){width="65%"}

[\[fig\_1\_clvsalpha\]]{#fig_1_clvsalpha label="fig_1_clvsalpha"}

![Drag coefficient vs. angle of attack at $U_{\infty}=80$
m/s.](1_cdvsalpha.eps){width="65%"}

[\[fig\_1\_cdvsalpha\]]{#fig_1_cdvsalpha label="fig_1_cdvsalpha"}

![Lift coefficient vs. drag coefficient at $U_{\infty}=80$
m/s.](1_clvscd.eps){width="65%"}

[\[fig\_1\_clvscd\]]{#fig_1_clvscd label="fig_1_clvscd"}

![$C_L/C_D$ vs. angle of attack at $U_{\infty}=80$
m/s.](1_clovercdvsalpha.eps){width="65%"}

[\[fig\_1\_clovercdvsalpha\]]{#fig_1_clovercdvsalpha
label="fig_1_clovercdvsalpha"}

![Lift coefficient distribution over half span at $\alpha=2$ degrees and
$U_{\infty}=80$ m/s.](1_clvsy.eps){width="65%"}

[\[fig\_1\_clvsy\]]{#fig_1_clvsy label="fig_1_clvsy"}

![Induced angle of attack distribution over half span at $\alpha=2$
degrees and $U_{\infty}=80$ m/s.](1_aivsy.eps){width="65%"}

[\[fig\_1\_aivsy\]]{#fig_1_aivsy label="fig_1_aivsy"}

Lifting Line Theory Analysis
============================

From the Kutta-Joukowski theorem, a bound vortex of strength $\Gamma$ (a
vortex filament which is somehow bound to a fixed location in the flow)
will experience a force $L=\rho U \Gamma$. In which $U$ and $\rho$ are
free stream velocity and density, respectively. We can replace a finite
wing of span $b$ with a bound vortex, extending from $y=-b/2$ to
$y=b/2$. However, according to Helmholtz's theorem, a vortex filament
cannot end in the fluid and has to continue to infinity or just end in a
wall. As a result assume that the vortex filament continues downstream
to infinity as two free vortices from wing tips. This setup is presented
in figure
[\[fig\_vortex\_anderson\_1\]](#fig_vortex_anderson_1){reference-type="ref"
reference="fig_vortex_anderson_1"} which is similar to a horseshoe and
is called a horseshoe vortex. Now consider the downwash $w$ induced by
the two trailing vortices along the span. Both of these vortices induce
a velocity pointing downward. The induced downwash can be described as
equation [\[eq\_downwash\_1\]](#eq_downwash_1){reference-type="ref"
reference="eq_downwash_1"}. The distribution of downwash along the span
of a wing with constant circulation of $\Gamma=4\pi$ (horizontal axis is
nondimentionalized with $b/2$) is presented in figure
[\[fig\_downwash\_distriburion\_span\_1\]](#fig_downwash_distriburion_span_1){reference-type="ref"
reference="fig_downwash_distriburion_span_1"}. Notice that downwash goes
to negative infinity at the tips.

![Replacement of the finite wing with a bound vortex
[@anderson2016fundamentals].](vortex_anderson_1.jpg){width="99%"}

[\[fig\_vortex\_anderson\_1\]]{#fig_vortex_anderson_1
label="fig_vortex_anderson_1"}

$$\label{eq_downwash_1}
w(y)=-\dfrac{\Gamma}{4\pi}\dfrac{b}{\left(\dfrac{b}{2}\right)^2-y^2}$$

![Downwash distribution over half span of a wing with constant
circulation.](wvsy.eps){width="65%"}

[\[fig\_downwash\_distriburion\_span\_1\]]{#fig_downwash_distriburion_span_1
label="fig_downwash_distriburion_span_1"}

Assume a vortex filament of strength $\Gamma$ is present in the space as
in figure
[\[fig\_bio\_savar\_1\]](#fig_bio_savar_1){reference-type="ref"
reference="fig_bio_savar_1"}. An element of this vortex filament will
induce a velocity $dV$ at point P which can be presented as in equation
[\[eq\_straight\_vortex\_filament\_cos\_0\]](#eq_straight_vortex_filament_cos_0){reference-type="ref"
reference="eq_straight_vortex_filament_cos_0"} according to Biot-Savart
law. Now imagine a finite straight piece of a bound vortex whom ends
make angles $\theta_1$ and $\theta_2$ with point P. In such conditions,
the induced velocity at point P will be as in equation
[\[eq\_straight\_vortex\_filament\_cos\_1\]](#eq_straight_vortex_filament_cos_1){reference-type="ref"
reference="eq_straight_vortex_filament_cos_1"}.

![The induced velocity $dV$ at P by an element of the vortex filament of
strength
$\Gamma$.](Vortex_filament_(Biot-Savart_law_illustration).png){width="50%"}

[\[fig\_bio\_savar\_1\]]{#fig_bio_savar_1 label="fig_bio_savar_1"}

$$\label{eq_straight_vortex_filament_cos_0}
d\vec{V}=\dfrac{\Gamma}{4\pi}\dfrac{d\vec{l}\times \vec{r}}{|r^3|}$$

$$\label{eq_straight_vortex_filament_cos_1}
V=-\dfrac{\Gamma}{4\pi r} (\cos(\theta_1)+\cos(\theta_2))$$

Now assume we have replaced an oblique wing at a sweep angle of
$\Lambda$ with a single horseshoe vortex as in figure
[\[fig\_oblique\_lifting\_1\]](#fig_oblique_lifting_1){reference-type="ref"
reference="fig_oblique_lifting_1"}. The induced velocity on any $y$ on
the span of the wing can be calculated as in equation
[\[eq\_ohshv\_1\]](#eq_ohshv_1){reference-type="ref"
reference="eq_ohshv_1"}. This equation can be rewritten in form of
equation [\[eq\_ohshv\_2\]](#eq_ohshv_2){reference-type="ref"
reference="eq_ohshv_2"}. The distribution of downwash along the span of
an oblique wing at different sweep angles of 0, 30, 45, and 60 degrees,
with constant circulation of $\Gamma=4\pi$ (horizontal axis is
nondimentionalized with $b/2$) is presented in figure
[\[fig\_downwash\_distriburion\_span\_2\]](#fig_downwash_distriburion_span_2){reference-type="ref"
reference="fig_downwash_distriburion_span_2"}. As seen in this figure,
downwash at tips goes to infinity again. This time however, we don't
have a symmetric distribution of downwash along the span. For an oblique
wing with non zero sweep, downwash increases on the right half span
(swept forward). However, downwash is less than the normal wing on the
outer part of the left half of the wing (swept back).

![Top view of an oblique horseshoe
vortex.](oblique_lifting.jpg){width="65%"}

[\[fig\_oblique\_lifting\_1\]]{#fig_oblique_lifting_1
label="fig_oblique_lifting_1"}

$$\label{eq_ohshv_1}
w(y)=-\dfrac{\Gamma}{4\pi (\dfrac{b}{2}+y)\cos(\Lambda)} (\cos(\dfrac{\pi}{2}+\Lambda)+\cos(0))-\dfrac{\Gamma}{4\pi (\dfrac{b}{2}-y)\cos(\Lambda)} (\cos(\dfrac{\pi}{2}-\Lambda)+\cos(0))$$

$$\label{eq_ohshv_2}
w(y)=-\dfrac{\Gamma}{4\pi\cos(\Lambda)} \left(\dfrac{2y\sin(\Lambda)+b}{\left(\dfrac{b}{2}\right)^2-y^2}\right)$$

![Downwash distribution over the span of an oblique wing with constant
circulation.](wvsy_oblique.eps){width="85%"}

[\[fig\_downwash\_distriburion\_span\_2\]]{#fig_downwash_distriburion_span_2
label="fig_downwash_distriburion_span_2"}

Downwash distribution due to a single horseshoe vortex does not simulate
a finite wing very well. Especially, downwash going to infinity at the
tips cannot be very realistic. Prandtl found a remedy for this issue and
that was to use a large number of horseshoe vortices to simulate the
effect more thoroughly. This concept is shown in figure
[\[fig\_lifting\_line\_2\]](#fig_lifting_line_2){reference-type="ref"
reference="fig_lifting_line_2"} with only 3 horseshoe vortices.
Derivation procedure of a traditional wing is presented in detail in
[@anderson2016fundamentals] and we are not going to repeat that here.
Instead, I will be deriving similar equations, only for an oblique wing
at a $\Lambda$ angle.

![Superposition of a finite number of horseshoe vortices along the
lifting line
[@anderson2016fundamentals].](superposition_lifting_line.jpg){width="85%"}

[\[fig\_lifting\_line\_2\]]{#fig_lifting_line_2
label="fig_lifting_line_2"}

Assume that we simulate the effect of a finite wing with an infinite
number of oblique horseshoe vortices as in figure
[\[fig\_oblique\_lifting\_2\]](#fig_oblique_lifting_2){reference-type="ref"
reference="fig_oblique_lifting_2"}. The induced velocity at point $y_o$
on the lifting line from a vortex element $d\Gamma=(d\Gamma/dy)dy$ at
position $y$ can be expressed as equation
[\[eq\_lifting\_1\]](#eq_lifting_1){reference-type="ref"
reference="eq_lifting_1"}. A simpler version of this equation is
presented in equation
[\[eq\_lifting\_2\]](#eq_lifting_2){reference-type="ref"
reference="eq_lifting_2"}. Now we have to integrate this equation over
the span of the wing as in equation
[\[eq\_lifting\_3\]](#eq_lifting_3){reference-type="ref"
reference="eq_lifting_3"}. The induced angle of attack is described as
the negative ratio of downwash to freestream velocity which is presented
in equation [\[eq\_lifting\_4\]](#eq_lifting_4){reference-type="ref"
reference="eq_lifting_4"}.

![Top view of many oblique horseshoe vortices making a finite
wing.](oblique_lifting_2.jpg){width="85%"}

[\[fig\_oblique\_lifting\_2\]]{#fig_oblique_lifting_2
label="fig_oblique_lifting_2"}

$$\label{eq_lifting_1}
dw=-\dfrac{(d\Gamma/dy)dy}{4\pi (y_o-y)\cos(\Lambda)} \left(\cos(\dfrac{\pi}{2}+\sign(y_o-y)\Lambda)+\cos(0)\right)$$

$$\label{eq_lifting_2}
dw=-\dfrac{(d\Gamma/dy)dy}{4\pi (y_o-y)\cos(\Lambda)} \left(-\sin(\sign(y_o-y)\Lambda)+1\right)$$

$$\label{eq_lifting_3}
w(y_o)=-\dfrac{1}{4\pi} \int_{-b/2}^{b/2} \dfrac{\left(-\sin(\sign(y_o-y)\Lambda)+1\right) (d\Gamma/dy)dy}{(y_o-y)\cos(\Lambda)}$$

$$\label{eq_lifting_4}
\alpha_i(y_o)=\dfrac{1}{4\pi U_{\infty}} \int_{-b/2}^{b/2} \dfrac{\left(-\sin(\sign(y_o-y)\Lambda)+1\right) (d\Gamma/dy)dy}{(y_o-y)\cos(\Lambda)}$$

Let's use a variable change as $y=\frac{b}{2}\cos(\theta)$ and
$y_o=\frac{b}{2}\cos(\theta_o)$ and rewrite equation
[\[eq\_lifting\_3\]](#eq_lifting_3){reference-type="ref"
reference="eq_lifting_3"} as follows.
$$w(\theta_o)=\dfrac{1}{4\pi} \int_{\pi}^{0} \dfrac{\left(-\sin(\sign(\theta_o-\theta)\Lambda)+1\right) (d\Gamma/dy)\sin(\theta)d\theta}{(\cos(\theta_o)-\cos(\theta))\cos(\Lambda)}$$
$$\label{eq_lifting_5}
w(\theta_o)=\dfrac{1}{4\pi} \int_{0}^{\pi} \dfrac{\left(-\sin(\sign(\theta_o-\theta)\Lambda)+1\right) (d\Gamma/dy)\sin(\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))\cos(\Lambda)}$$
$d\Gamma/dy$ can be rewritten in the following form.
$$\dfrac{d\Gamma}{dy}=\dfrac{d\Gamma}{d\theta} \dfrac{d\theta}{dy}=-\dfrac{d\Gamma}{d\theta}  \dfrac{1}{\frac{b}{2}\sin(\theta)}$$
As a result, equation
[\[eq\_lifting\_5\]](#eq_lifting_5){reference-type="ref"
reference="eq_lifting_5"} can be changed as follows.
$$w(\theta_o)=-\dfrac{1}{2\pi b} \int_{0}^{\pi} \dfrac{\left(-\sin(\sign(\theta_o-\theta)\Lambda)+1\right) (d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))\cos(\Lambda)}$$
$$w(\theta_o)=-\dfrac{1}{2\pi b \cos(\Lambda)} \int_{0}^{\pi} \dfrac{\left(-\sin(\sign(\theta_o-\theta)\Lambda)+1\right) (d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))}$$
$$w(\theta_o)=-\dfrac{1}{2\pi b \cos(\Lambda)} \left[ \int_{0}^{\pi} \dfrac{ (d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))}   - \int_{0}^{\pi} \dfrac{ \sin(\sign(\theta_o-\theta)\Lambda) (d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))}   \right]$$
$$\begin{split}
w(\theta_o)=-\dfrac{1}{2\pi b \cos(\Lambda)} &\left[ \int_{0}^{\pi} \dfrac{ (d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))}   - \sin(\Lambda)  \int_{0}^{\theta_o} \dfrac{(d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))}   \right.\\
&\left. +\sin(\Lambda)  \int_{\theta_o}^{\pi} \dfrac{(d\Gamma/d\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))} \right]
\end{split}$$ For an elliptical circulation distribution of
$\Gamma=\Gamma_o \sin(\theta)$ we can integrate to a point.
$$\begin{split}
w(\theta_o)=-\dfrac{\Gamma_o }{2\pi b \cos(\Lambda)} &\left[ \pi   - \sin(\Lambda) \left( \int_{0}^{\theta_o} \dfrac{\cos(\theta) d\theta}{(\cos(\theta)-\cos(\theta_o))} - \int_{\theta_o}^{\pi} \dfrac{\cos(\theta)d\theta}{(\cos(\theta)-\cos(\theta_o))} \right) \right]
\end{split}$$

Unfortunately, I have not been able to find a solution for the final
integration yet. Turns out this integral (even for the simple case of
$\Lambda=0$) is very difficult to calculate. A proof of equation
[\[eq\_lifting\_6\]](#eq_lifting_6){reference-type="ref"
reference="eq_lifting_6"} is presented in appendix E of
[@karamcheti1980principles]. As a result, I will just use numerical
integration to find the downwash. It is important to mention that even
numerical integration of this equation is not straightforward. Now
imagine an oblique wing with an elliptic lift distribution of
$\Gamma=\Gamma_o \sin(\theta)$ in which $\Gamma_o=2\pi b$. The
distribution of downwash along the span of an elliptic oblique wing at
different angles of sweep of 0, 30, 45, and 60 degrees is presented in
figure
[\[fig\_downwash\_elliptic\_oblique\_1\]](#fig_downwash_elliptic_oblique_1){reference-type="ref"
reference="fig_downwash_elliptic_oblique_1"}.

As seen in figure
[\[fig\_downwash\_elliptic\_oblique\_1\]](#fig_downwash_elliptic_oblique_1){reference-type="ref"
reference="fig_downwash_elliptic_oblique_1"}, we have mostly favorable
induced velocity on the right half span for non zero oblique. On the
other hand, downwash on the left half span is more severe than the case
with zero oblique angle. increasing the oblique angle, results in larger
changes in downwash velocity. Interesting to note that downwash changes
sign on the right half of the wing.

$$\label{eq_lifting_6}
\int_{0}^{\pi} \dfrac{\cos(n\theta)d\theta}{\cos(\theta)-\cos(\theta_o)}=\pi\dfrac{\sin(n\theta_o)}{\sin(\theta_o)}$$

![Downwash distribution along the span of an elliptic oblique
wing.](wvsy_oblique_2.eps){width="65%"}

[\[fig\_downwash\_elliptic\_oblique\_1\]]{#fig_downwash_elliptic_oblique_1
label="fig_downwash_elliptic_oblique_1"}

Total lift of an oblique wing with elliptic lift distribution can be
calculated using the following procedure.
$$L=\rho_{\infty} U_{\infty} \cos(\Lambda) \Gamma = \rho_{\infty} U_{\infty} \cos(\Lambda) \Gamma_o \int_0^{\pi} \sin^2(\theta)d\theta=\rho_{\infty} U_{\infty} \cos(\Lambda) \Gamma_o  \dfrac{b}{4} \pi$$
Assuming an elliptic lift distribution we have the following.
$$L(\theta)=L_o sin(\theta)$$
$$L_o=\rho_{\infty} U_{\infty} \cos(\Lambda) \Gamma_o$$
$$D_i(\theta)=L\sin(\alpha_i)=\rho_{\infty} U_{\infty} \cos(\Lambda) \Gamma_o \sin(\theta) \sin(\dfrac{-w(\theta)}{U_{\infty}})$$
Assume $\Gamma_o=2\pi b$ and $U_{\infty}=300$ and plot
$\dfrac{D_i(\theta)}{\rho_{\infty} U_{\infty} \Gamma_o}$ as in figure
[\[fig\_induceddrag\_oblique\_1\]](#fig_induceddrag_oblique_1){reference-type="ref"
reference="fig_induceddrag_oblique_1"}. This figure shows that for non
zero oblique angle on the outer section of the right half span, we are
getting induced drag in the direction of movement. Integrating these
results which are presented in table
[\[table\_oblique\_induced\_drag\_1\]](#table_oblique_induced_drag_1){reference-type="ref"
reference="table_oblique_induced_drag_1"}, shows that the total induced
drag decreases with increasing oblique angle :) The same test is carried
out at a free stream velocity of at $U_{\infty}=100$ and the results are
presented in figure
[\[fig\_induceddrag\_oblique\_2\]](#fig_induceddrag_oblique_2){reference-type="ref"
reference="fig_induceddrag_oblique_2"} and table
[\[table\_oblique\_induced\_drag\_2\]](#table_oblique_induced_drag_2){reference-type="ref"
reference="table_oblique_induced_drag_2"}. Again, at higher angles of
oblique, the induced drag is reduced. An important thing to note in
figures
[\[table\_oblique\_induced\_drag\_1\]](#table_oblique_induced_drag_1){reference-type="ref"
reference="table_oblique_induced_drag_1"} and
[\[table\_oblique\_induced\_drag\_2\]](#table_oblique_induced_drag_2){reference-type="ref"
reference="table_oblique_induced_drag_2"} is that the induced drag is
constant at the center of span with changing $\Lambda$.

![Nondimensionalized induced drag distribution along the span of an
elliptic oblique wing at
$U_{\infty}=300$.](Divsy_oblique_2.eps){width="75%"}

[\[fig\_induceddrag\_oblique\_1\]]{#fig_induceddrag_oblique_1
label="fig_induceddrag_oblique_1"}

![Nondimensionalized induced drag distribution along the span of an
elliptic oblique wing at
$U_{\infty}=100$.](Divsy_oblique_3.eps){width="75%"}

[\[fig\_induceddrag\_oblique\_2\]]{#fig_induceddrag_oblique_2
label="fig_induceddrag_oblique_2"}

[\[table\_oblique\_induced\_drag\_1\]]{#table_oblique_induced_drag_1
label="table_oblique_induced_drag_1"}

   $\Lambda$ \[degrees\]   Total induced drag
  ----------------------- --------------------
             0                 0.0164236
            30                 0.0164083
            45                 0.0163848
            60                 0.0163361

  : Total nondimensionalized induced drag vs. oblique angle of sweep at
  $U_{\infty}=300$.

[\[table\_oblique\_induced\_drag\_2\]]{#table_oblique_induced_drag_2
label="table_oblique_induced_drag_2"}

   $\Lambda$ \[degrees\]   Total induced drag
  ----------------------- --------------------
             0                  0.049264
            30                  0.049140
            45                  0.048928
            60                  0.048419

  : Total nondimensionalized induced drag vs. oblique angle of sweep at
  $U_{\infty}=100$.

Such analysis on oblique wings are not new and there are a few previous
articles focusing on this matter. Cheng in 1978 [@cheng1978lifting],
extended Prandtl's approach to planar wings including curved and swept
centerlines. Further in 1980 [@cheng1980oblique], Cheng presented a
transonic flow theory of thin, oblique wing of high aspect ratio, which
permitted a delineation of the influence of wing sweep, the centerline
curvature, and other three-dimensional effects on the nonlinear mixed
flow in the framework of small disturbance theory. They carried out
upwash corrections which includes the influence of both the near and far
wakes, as well as the local curvature of the centerline.

Far Field Analysis and the Trefftz Plane
========================================

![control volume around a finite wing.](treftz_plane_1.jpg){width="85%"}

[\[fig\_treftz\_plane\_1\]]{#fig_treftz_plane_1
label="fig_treftz_plane_1"}

Consider an inviscid, incompressible potential flow around a wing and
define a control volume surrounding the body as presented in figure
[\[fig\_treftz\_plane\_1\]](#fig_treftz_plane_1){reference-type="ref"
reference="fig_treftz_plane_1"}. Upstream velocity is $U_{\infty}$ and
in x direction which means drag is in x direction as sell. We can
utilize the momentum integral in x direction to find the drag (induced
drag in this case).
$$\iint_{S_{\text{body}+S_{\infty}}} \rho \vec{V}\vec{V}\cdot \vec{n} dS=-\iint_{S_{\text{body}+S_{\infty}}} P \vec{n} dS$$
On the body we have $\vec{V}\cdot \vec{n}=0$.
$$\iint_{S_{\infty}} \rho \vec{V}\vec{V}\cdot \vec{n} dS=-\iint_{S_{\text{body}+S_{\infty}}} P \vec{n} dS$$
On the body we also have
$-\iint_{S_{\text{body}}} P \vec{n} dS=(\text{force of body acting on the fluid})$.
The opposite of this force is acting on the body (from fluid) and has
three components, drag in x direction, lift in z direction, and side
force in y direction.
$$D \hat{i} +Y \hat{j} +L \hat{k}=\iint_{S_{\text{body}}} P \vec{n} dS$$
As a result:
$$D \hat{i} +Y \hat{j} +L \hat{k}=-\iint_{S_{\infty}} \rho \vec{V}\vec{V}\cdot \vec{n} dS-\iint_{S_{\infty}} P \vec{n} dS$$
The drag component can be extracted as follows.
$$D=-\iint_{S_{\infty}} \rho u \vec{V}\cdot \vec{n} dS-\iint_{S_{\infty}} P \vec{n}\cdot\vec{i} dS$$
Now we can apply Bernoulli equation to eliminate the pressure.
$$P=P_{\infty}+\dfrac{1}{2} \rho U_{\infty}^2-\dfrac{1}{2} \rho(u^2+v^2+w^2)$$
$$D=-\iint_{S_{\infty}} \rho u \vec{V}\cdot \vec{n} dS-\iint_{S_{\infty}} \left[P_{\infty}+\dfrac{1}{2} \rho U_{\infty}^2-\dfrac{1}{2} \rho(u^2+v^2+w^2)\right] \vec{n}\cdot\vec{i} dS$$
We know that
$\iint_{S_{\infty}} \left[P_{\infty}+\dfrac{1}{2} \rho U_{\infty}^2\right] \vec{n}\cdot\vec{i} dS=0$.
$$D=-\iint_{S_{\infty}} \rho u \vec{V}\cdot \vec{n} dS+\iint_{S_{\infty}} \dfrac{1}{2} \rho(u^2+v^2+w^2) \vec{n}\cdot\vec{i} dS$$
Now we can rewrite the free stream velocity into an integral part and
perturbation. $$\begin{cases}
u=U_{\infty} +\hat{u}\\[10 pt]
v=0+\hat {v}\\[10 pt]
w=0+\hat{w}
\end{cases}$$ In which $\hat{u}$, $\hat{v}$, and $\hat{w}$ are
perturbation velocities (not necessarily small). Let's rewrite the drag
force with these new velocities.
$$D=- \rho \iint_{S_{\infty}}(U_{\infty}+\hat{u}) \vec{V}\cdot \vec{n} dS+\dfrac{1}{2} \rho\iint_{S_{\infty}} (U_{\infty}^2+2U_{\infty}\hat{u} +\hat{u}^2+\hat{v}^2+\hat{w}^2) \vec{n}\cdot\vec{i} dS$$
Again, we know that
$\rho \iint_{S_{\infty}} U_{\infty} \vec{V}\cdot \vec{n} dS=0$ and
$\dfrac{1}{2} \rho\iint_{S_{\infty}} U_{\infty}^2 \vec{n}\cdot\vec{i} dS=0$.
$$D=- \rho \iint_{S_{\infty}}\hat{u} \vec{V}\cdot \vec{n} dS+\dfrac{1}{2} \rho\iint_{S_{\infty}} (2U_{\infty}\hat{u} +\hat{u}^2+\hat{v}^2+\hat{w}^2) \vec{n}\cdot\vec{i} dS$$
Perturbation velocities on all control volume boundaries far away from
the wing are zero except for the downstream plane (Trefftz plane
$S_\text{T}$).
$$D=- \rho \iint_{S_\text{T}}\hat{u} \vec{V}\cdot \vec{n} dS+\dfrac{1}{2} \rho\iint_{S_\text{T}} (2U_{\infty}\hat{u} +\hat{u}^2+\hat{v}^2+\hat{w}^2) \vec{n}\cdot\vec{i} dS$$
$$D=- \rho \iint_{S_\text{T}}\hat{u} (U_{\infty}+\hat{u}) dS+\dfrac{1}{2} \rho\iint_{S_\text{T}} (\hat{u}^2+\hat{v}^2+\hat{w}^2)  dS    +   \rho U_{\infty} \iint_{S_\text{T}} \hat{u} dS$$
Eliminate zero terms.
$$D=- \rho \iint_{S_\text{T}}\hat{u} \hat{u} dS+\dfrac{1}{2} \rho\iint_{S_\text{T}} (\hat{u}^2+\hat{v}^2+\hat{w}^2)  dS$$
$$D=\dfrac{1}{2} \rho\iint_{S_\text{T}} (-\hat{u}^2+\hat{v}^2+\hat{w}^2)  dS$$
As a final note, we know that trailing vortices far downstream are in x
direction which means that $\hat{u}=0$ on Trefftz plane.
$$\label{eq_trefftz_1}
D=\dfrac{1}{2} \rho\iint_{S_\text{T}} (\hat{v}^2+\hat{w}^2)  dS$$
Equation [\[eq\_trefftz\_1\]](#eq_trefftz_1){reference-type="ref"
reference="eq_trefftz_1"} shows that the induced drag of a finite wing
is in fact the kinetic energy transferred into the cross flow (i.e. the
trailing vortices).

using Gauss's theorem, induced drag can be expressed as a line integral
over the wake itself.
$$D=-\dfrac{1}{2} \rho\oint_{\text{wake}} \Gamma V_n  dl$$ This
simplifies the calculation of drag. $V_n$ is the downwash at the wake
far downstream of the wing. As a result, if the wake of any finite wing
(including swept and oblique ones) is known we can calculate the induced
drag.

Nonplanar Wakes
---------------

All of the comments above apply to nonplanar wings as well as to simple
planar ones. But we must be careful about the assumed wake shape when
evaluating forces in the far field. The integrals above actually give
the force on the wing and wake combination. Of course, in reality, there
is no force on the wake sheet, but if we assume a shape a priori, it is
not likely to be a force-free wake. However, since forces act in a
direction perpendicular to the vortex, extending wakes streamwise always
yields a drag free wake and nearly correct answers for drag using far
field methods.

Munk's Stagger Theorem
----------------------

The result that the drag of a lifting system depends only on the
distribution of circulation shed into the wake leads to some very useful
results in classical aerodynamics. Perhaps the most useful of these is
called Munk's stagger theorem [@larrabee1975trim]. It states that: *The
total induced drag of a system of lifting surfaces is not changed when
the elements are moved in the streamwise direction.* The theorem applies
when the distribution of circulation on the surfaces is held constant by
adjusting the surface incidences as the longitudinal position is varied.
This implies that the drag of an elliptically loaded swept wing (at the
same span) is the same as that of an unswept wing. It also is very
useful in the study of canard airplanes for which the canard downwash on
the wing is quite complicated. Moving the canard very far behind the
wing does not change the drag, but makes its computation much easier.
One may use the stagger theorem to prove several other useful results.
One of these is the mutual induced drag theorem [@demasi2017minimum]
which states that: *The interference drag caused by the downwash of one
wing on another is equal to that produced by the second wing on the
first, when the surfaces are unstaggered (at the same streamwise
location).* These results are especially useful in analyzing multiple
lifting surfaces.

Conclusion
==========

The present study tried to shine an oblique light on the drag reduction
mechanisms of oblique wings. We used XFLR5 and lifting line analysis to
characterize the phenomenon in action. As a benchmark, we looked at NASA
AD-1 (Ames-Dryden-1) aircraft which utilized a wing that could be
pivoted obliquely from zero to 60 degrees during flight. R.T. Jones of
NASA Ames Research Center has conducted some of the earliest theoretical
studies on this subject, beginning in the 1950s. Further, there has been
a number of test flights to prove the feasibility and performance of
oblique wings. We presented a historical review of oblique wing
airplanes and other oblique wing studies. Then XFLR5 software was
utilized to analyze the characteristics and performance of NASA AD-1
wing at zero sweep. I also utilized lifting line theory to analyze the
effect of oblique angle on the induced drag. Our lifting line analysis
showed a reduction in induced drag with increasing oblique angle.
Unfortunately, I don't have enough time to study the effects of flow
compressibility on the performance of oblique wings. At transonic and
supersonic flights, wave drag is the dominant component of total drag. A
significant advantage of oblique wing arrangements for supersonic flight
is that they distribute the lift over about twice the wing length
compared to a conventional, symmetrically swept wing. This reduces lift
dependent wave drag by a factor of 4 and volume dependent wave drag by a
factor of 16.

[\[endOfDoc\]]{#endOfDoc label="endOfDoc"}

[^1]: The fineness ratio is the ratio of the length of a body to its
    maximum width
