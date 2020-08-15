# Mechanical setup
This is the mechanical part of the experiment. In order to detect the change in the wavelength of light, we need a mirror moving as fast as possible. If the speed is too slow, no noticeable difference will be measured.
Of course, this is not easy. But after several failures, I found a way of doing it that should work.

An slider + rail was attached to a 2x4 wood that makes a reasonable (but far from perfect) base for the rail. 
The rail should not be tightened, or the rail may conform to any curvature of the wood.
A Nema 23 stepper motor plus some 2GT pulleys + belts make a speed "increaser" (yes, the opposed to a speed reducer).
That way, the motor can work at low speed (where it is stronger) while the slider moves 9 times faster.
The motor is powerful enough to generate an appreciable speed on the slider, but the acceleration became stronger too in order to achieve such speeds in a 50 cm rail.
Under certain acceleration, the slider hits the hard stops because of the strong force developed.

# Motor Control
The stepper control is achieved using an arduino nano, and the TAL library. This controller sends the step and directions signals, and receive the limit switch signal.

It is possible to attach the control to the same assembly of the motor, so it became a single unit. This sounds good, as we will be able to have a single functional unit, so we just have to provide 110 volts and it will work. However, by doing this, the controller will be separated of other controllers of the system, and communication from the PC to the motor control will require the PC to be close both to the control box and to the slider. If instead we keep the controller inside the control box, then only the control box should be located next to the PC, what should reduce the clutter.


(pendientes)
-agregar fotos
-documentar motor, ensamble, video funcionando, forma de soportarlo (motor, incrementador).
-Programa que lo controla (link a él). Programa puede cambiar con el tiempo.
-Pensar si hay que separar control de motor de caja de control (me suena que no, pero revisar)
  -No, porque la caja de ctrol debe estar cerca al cpu por distintas razones, lo que nos permite comunicarnos con el control del motor también.
