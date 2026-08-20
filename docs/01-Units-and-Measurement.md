# Chapter 1 — Units, Measurement, and Estimation

*Needs from earlier chapters: nothing. Start here.*

Physics is quantitative. Before any equations, you need three habits: always
carry units, check dimensions, and estimate before you calculate.

## 1.1 SI base units

Everything in mechanics is built from three base units:

| Quantity | Unit | Symbol |
|----------|------|--------|
| Length | metre | m |
| Mass | kilogram | kg |
| Time | second | s |

Every other mechanical quantity is a combination:

| Quantity | Unit | In base units |
|----------|------|---------------|
| Velocity | m/s | m·s⁻¹ |
| Acceleration | m/s² | m·s⁻² |
| Force | newton (N) | kg·m·s⁻² |
| Energy / work | joule (J) | kg·m²·s⁻² |
| Power | watt (W) | J/s = kg·m²·s⁻³ |
| Pressure | pascal (Pa) | N/m² |
| Frequency | hertz (Hz) | s⁻¹ |

Common prefixes: k (kilo, 10³), M (mega, 10⁶), G (giga, 10⁹),
m (milli, 10⁻³), µ (micro, 10⁻⁶), n (nano, 10⁻⁹).

**Watch out:** kg is the base unit, not g. And a kilowatt-hour (kWh) is a unit
of *energy*, not power: 1 kWh = 1000 W × 3600 s = 3.6 × 10⁶ J = 3.6 MJ.

## 1.2 Unit conversion — the factor method

Multiply by fractions equal to 1 until the units you don't want cancel.

**Worked example.** Convert 60 km/h to m/s.

    60 km/h × (1000 m / 1 km) × (1 h / 3600 s) = 60 × 1000/3600 m/s ≈ 16.7 m/s

Handy shortcut: **km/h ÷ 3.6 = m/s**. So 36 km/h = 10 m/s, 72 km/h = 20 m/s.
This one is worth memorising — traffic-speed problems come up constantly.

## 1.3 Dimensional analysis — the free error detector

Every valid physics equation must have the same dimensions on both sides. Write
dimensions as [L] length, [M] mass, [T] time.

**Worked example.** Is `d = ½at²` dimensionally sensible?
Right side: [L·T⁻²]·[T²] = [L]. Left side: [L]. ✓ Consistent.

Is `v = at²` sensible? Right side: [L·T⁻²]·[T²] = [L] — that's a length, not a
velocity [L·T⁻¹]. ✗ Wrong, no calculation needed.

Dimensional analysis can't catch dimensionless mistakes (a missing ½, a wrong
sign), but it catches a huge fraction of algebra slips for free. Use it on
every result you derive.

## 1.4 Significant figures and honest precision

- Your answer can't be more precise than your worst input. If a car's mass is
  "about 1500 kg", quoting energy as 4417.238 J is fiction — say 4.4 kJ.
- Keep extra digits *during* a calculation; round only at the end.
- In rough engineering estimates, 2 significant figures is usually right.

## 1.5 Order-of-magnitude estimation (Fermi problems)

Before computing anything, guess the answer to within a factor of 10. If the
computed result disagrees wildly with your estimate, one of them is wrong —
and it's usually the calculation (a unit slip, a lost factor of 1000).

**Worked example.** How much kinetic energy does a car at urban speed carry?
Car ≈ 1000–2000 kg, urban speed ≈ 10–15 m/s. KE = ½mv² ≈ ½ × 1500 × 12²
≈ 10⁵ J ≈ 100 kJ. So when you later compute a speed-bump harvester yield of
50–300 J per pass, you immediately know it's a tiny slice (~0.1–0.3%) of the
car's kinetic energy — which passes the sanity check: the bump barely slows
the car.

## Common pitfalls

- Mixing km/h and m/s inside one formula. Convert everything to SI *first*.
- Treating kW and kWh as interchangeable. kW is a rate; kWh is an amount.
- Dropping units mid-calculation and re-attaching the wrong ones at the end.
  Carry units through every line.

## Practice problems

1. Convert 100 km/h to m/s.
2. A 60 W streetlight runs 12 h per night. How many joules per night? How many
   kWh?
3. Check dimensionally: could `T = 2π√(L/g)` be a valid formula for the period
   of a pendulum (T in seconds, L in metres)?
4. Estimate the number of car passes per year over a bump carrying
   10,000 vehicles/day.

??? success "Answers"

    1. 100 / 3.6 ≈ **27.8 m/s**.
    2. 60 W × 12 × 3600 s = **2.59 MJ** = 60 W × 12 h = 720 Wh = **0.72 kWh**.
    3. √(L/g) has dimensions √([L]/[L·T⁻²]) = √([T²]) = [T]. ✓ Yes, dimensionally
       valid (2π is dimensionless).
    4. 10,000 × 365 ≈ **3.7 million passes/year**.

