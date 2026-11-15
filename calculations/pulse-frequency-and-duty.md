# Pulse frequency and cycle timing

All numbers below are synthetic worked examples, not measured R15 data.

For a pulse rate f in Hz and p pulses/revolution:

`RPM = 60 × f / p`.

Example: `60 × 100 Hz / 1 pulse/revolution = 6000 RPM`.

The selected SAN firmware assumes one pulse/revolution for a generated bench test. Actual crank, tach and injector waveforms can have different event counts; determine the physical meaning before applying the equation.

For an ideal four-stroke cycle with one complete cycle per two crank revolutions:

`cycle period [ms] = 120000 / RPM`.

At hypothetical 6000 RPM: `120000 / 6000 = 20 ms`.

If a hypothetical injector is commanded once per full cycle for 3 ms, the occupied fraction is `3 / 20 × 100 = 15%`. This calculation depends on event strategy and effective electrical timing. It does not establish injector flow, delivered mass, air-fuel ratio or suitable calibration. Multiple pulses and dead time require separate treatment.

Dimensional checks: frequency × 60 converts revolutions/second to revolutions/minute after dividing pulses/revolution; two revolutions × 60000 ms/minute gives the cycle numerator 120000.
