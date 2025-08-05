### Understanding Maxon Combinatinos
- Motor + gears
- Controllers
- Gears
- Driving Motors with MCU and ecosystem
### Undertsand Replacment
- T Gimbal motor
- Controllers
- Gear or direct
- Driving Motors with MCU and ecosystem ( ODrive )
---

- Create Complete structure of MTM

------

### Questions

- Check if MTM actually drives motors ? Or its just by the users ?
- Why FOC
- Certifications
- Plug and play if we shift to other motors( Maxon , T motors )



### Practical Checklist for Replacing an Actuator Unit:
- [ ] : Draw current design of Motors , Motor Drivers , Sensors flow , characterisitcs etc.
- [] : Alternative design of Motors , Motor Drivers , Sensors flow
- [ ] : Draw compare mechanical cad design changes required for new motor replacments


- compare in detail the maxon and gimbal motors
    - Peak , Stall, Continuous torque
    - Dimensions , Weights
    - Drivers , encoders resoltion
    - Costs


- If we upgradee cubemars to maxon later , driver compaitlibity
- maxon motors different types driver compatibillty
- calculate total torque required for each axis and find motors
- Find things that w amissing
- Smallest mvomeent , stablility , accuracy
- Drivers ,
- Reflected inertia - bldc manual rotation inertia as we are driving passively
    - How to drive contionusly without resistance


- When docter moves the MTM , electricity is there product is on , Reduce friction in motion because bldc moves poles to poles.


- Friction componensation , gear vs direct drive, -> feel of surgeon.
---
- Cogging torque = magnetic “stickiness” that causes jumps when rotating the motor manually.
- With FOC you can
    - Don’t resist movement at all
    - Hold this position gently
    - Soft spring or haptic feedback
- What you want:
    - When user moves the arm → no resistance, smooth motion
    - When user lets go → hold position gently
    - When user reaches a limit → resist further movement with controlled force

- How it’s achieved with BLDC + FOC:
    - Zero torque mode → Cancels cogging, friction, and back EMF
    - Active torque holding → Apply light torque to maintain joint angles
    - Soft limits → At angle thresholds, increase torque to push back
    - No gears → No reflective inertia → Very natural feel
- How much friction and inertia when its holding
----

Maxon Moto ECX Flat 22 - 28mNM \ 150 $
ECX Flat 32 94 mNm \ 178
ECX Flat 40 200 mNm \ 178


----
- Calculate torques because of MTM link size
----
