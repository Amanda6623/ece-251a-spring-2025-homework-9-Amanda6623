# ece-251a-spring-2025-homework-9-Amanda6623

## 1 (textbook problem 1.5)
<§1.6> Consider three different processors P1, P2, and P3 executing the same instruction set. P1 has a 3 GHz clock rate and a CPI of 1.5. P2 has a 2.5 GHz clock rate and a CPI of 1.0. P3 has a 4.0 GHz clock rate and has a CPI of 2.2. \
#1.a. Which processor has the highest performance expressed in instructions per second? \
P1: 3/1.5 = 2 \
P2: 2.5/1 = 2.5 \
P3: 4/2.2 = 1.82 \
P2 has the highest performance.

#1.b. If the processors each execute a program in 10 seconds, find the number of cycles and the number of instructions. \
P1: $ 3 * 10^{10} $ cycles, $ 2 * 10^{10} $ instructions \
P2: $ 2.5 * 10^{10} $ cycles, $ 2.5 * 10^{10} $ instructions \
P3: $ 4 * 10^{10} $ cycles, $ 1.82 * 10^{10} $ instructions 

#1.c. We are trying to reduce the execution time by 30% but this leads to an increase of 20% in the CPI. What clock rate should we have to get this time reduction? \
$ 7/10 CPUtime = Instructions*1.2CPI/newClockrate $ \
$ newClockrate = 1.2*10/7 oldClockrate = 1.71 oldClockrate $

## 2  (textbook problem 1.7)
<§1.6> Consider two different implementations of the same instruction set architecture. The instructions can be divided into four classes according to their CPI (class A, B, C, and D). P1 with a clock rate of 2.5 GHz and CPIs of 1, 2, 3, and 3, and P2 with a clock rate of 3 GHz and CPIs of 2, 2, 2, and 2. \
Given a program with a dynamic instruction count of 1.0E6 instructions divided into classes as follows: 10% class A, 20% class B, 50% class C, and 20% class D, which is faster: P1 or P2? \
#2a. What is the global CPI for each implementation? \
P1: 1(.1) + 2(.2) + 3(.5) + 3(.2) = 2.6 \
P2: 2(.1) + 2(.2) + 2(.5) + 2(.2) = 2 

#2b. Find the clock cycles required in both cases. \
P1: 2.6 * 1.0E6 = $ 2.6 * 10^6 $\
P2: 2 * 1.0E6 = $ 2 * 10^6 $

Time for P1 = $ 2.6 * 10^6 / (2.5 * 10^9) = 0.00104 $ \
Time for P2 = $ 2 * 10^6 / (3 * 10^9) = 0.00067$ \
P2 is faster

## 3 (textbook problem 1.12)
The results of the SPEC CPU2006 bzip2 benchmark running on an AMD Barcelona has an instruction count of 2.389E12, an execution time of 750 s, and a reference time of 9650 s. \
#3.a <§§1.6, 1.9> Find the CPI if the clock cycle time is 0.333 ns. \
$ 750 = 2.389E12 * CPI * 0.333 * 10^{-9} $ \
CPI = 0.942

#3.b <§§1.6, 1.9> Find the increase in CPU time if the number of instructions of the benchmark is increased by 10% without affecting the CPI. \
$ CPU time = 750 * 1.1 = 825s$ \
increase = 75s

#3.c <§§1.6, 1.9> Find the increase in CPU time if the number of instructions of the benchmark is increased by 10% and the CPI is increased by 5%. \
$ CPU time = 750 * 1.1 * 1.05 = 866.25 s $ \
increase = 116.25s

#3.d <§1.6> Suppose that we are developing a new version of the AMD Barcelona processor with a 4 GHz clock rate. We have added some additional instructions to the instruction set in such a way that the number of instructions has been reduced by 15%. The execution time is reduced to 700 s and the new SPECratio is 13.7. Find the new CPI. \
$ 700 = 0.85(2.389E12) * CPI / (4*10^9) $ \
CPI = 1.38
