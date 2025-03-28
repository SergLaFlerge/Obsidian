# Measurement of the Positive Muon Anomalous Magnetic Moment to 0.20 ppm

This paper is self-explanatory. Physicists at  Fermilab present a new measurement of the positive muon magnetic moment  (defined $a_{\mu}\equiv (g_{\mu-2)/2}$) using data collected from the 2019 and 2020 runs of the $g-2$ experiment. Thanks to better running conditions, a more stable beam, and an improved knowledge of the magnetic field weighted by the muon distribution $\tilde{\omega}'_{p}$ as well as the anomalous precession frequency corrected for beam dynamics, the systematic error was reduced by more than a factor of 2 compared to the 2018 run. This time around, they determined $a_{\mu}= 116\;592\; 057 (25)\times 10^{-11}$ $(0.21)$ppm. They combined this result with the previous 2018 **Run-1 citation obtained** result to obtain $116 \; 592 \; 059 (22)\times 10^{-11}$ $(0.20)$ppm. The world average is now given at $a_{\mu}(\text{exp}) = 116 \; 592 \; 059 (22)\times 10^{-11}$ $(0.19)$ppm, which represents a factor of two improvement in precision.

## Introduction

We care about this because precision measurements of things like the muon magnetic anomaly, henceforth called $a_{\mu}$, provide very good tests for the standard model (SM). This is because $a_{\mu}$ can be predicted with high precision theoretically. Any deviation in the measurements compared to theoretical predictions may point to new physics beyond the SM.

Using data collected in 2019 (Run-2) and 2020 (Run-3), the team at Fermilab produced a new measurement for $a_{\mu}$. Compared to previous measurements (Run-1), there was a four-fold increase in detected positrons thanks to improvements made as mentioned in the abstract. All these factors lead to more than a factor of 2 reduction in systematic uncertainties, which surpassed the experiment's design goal.

Run-1 publications describe the principle of the experiment, as well as giving previous results and experimental details.

### Reading Around the Paper

Need more background on why this measurement is important, as well as a description of what $a_{\mu}$ is. No need to go into more detail on the method until we get to the method section.

**Cite Fermilab webpage**

## Method

> [!PDF|note] [[L99-Paper Review.pdf#page=2&selection=242,0,267,47&color=note|L99-Paper Review, p.2]]
> > The experiment uses $3.1 GeV/c$ polarized muons produced at the Fermilab Muon Campus **citation needed**. Muons are injected into a $7.112$-m radius storage ring that was moved, and significantly upgraded, from the BNL experiment **Fermilab website citation**.

The key components of the storage ring are kicker magnets that direct the injected muons onto the central orbit of the storage ring, and the electrostatic quadrupoles (ESQs) that provide vertical focusing of the stored beam.

> [!PDF|note] [[L99-Paper Review.pdf#page=3&selection=4,0,54,26&color=note|L99-Paper Review, p.3]]
> > We incorporated major instrumental improvements with respect to Run-1. Resistors in the high-voltage feedthroughs for the ESQ system that were damaged in Run-1 were replaced before Run-2. This upgrade greatly improved transverse beam stability. Thermal insulation was added to the storage ring magnet before Run-2 to remove diurnal temperature variations. Increased cooling power and improved air circulation in the experimental hall installed before Run-3 reduced seasonal temperature variations. The magnitude and reliability of the kicker field were improved between Run-1 and Run-2, and again within Run-3. Because of these improvements, the data are analyzed in three sets—Run-2, Run-3a, and Run-3b.
> 
>  Worth mentioning, as this led to significant improvements.

## Analysis

The muon magnetic anomaly is calculated from [15]:

$$
a_{\mu} = \frac{\omega_{a}}{\tilde{\omega}'_{p}(T_{r})}\frac{\mu'_{p}(T_{r})}{\mu_{e}(H)}\frac{\mu_{e}(H)}{\mu_{e}}\frac{m_{\mu}}{m_{e}}\frac{g_{e}}{2},
$$

 where the important bits are $T_{r}= 34.7^{\circ}$C  — the temperature at which the shielded proton-to-electron magnetic moment is measured — and the ratio

$$
\mathcal{R}'_{\mu} = \frac{\omega_{a}}{\tilde{\omega}'_{p}(T_{r})}
$$

— which is the ratio composed of the two measured quantities. $\mathcal{R}'_{\mu}$ must be corrected as there are numerous effects which must be accounted for. These correction shift the value of $\mathcal{R}'_{\mu}$ by $+ 622$ ppb in total. The corrections in $\mathcal{R}'_{\mu}$ can be written as a ratio of measured quantities as well as the correction terms as

$$
\mathcal{R}'_{\mu} \approx\frac{f_{\text{ clock}}\cdot \omega^{m}_{a}(1 + C_{e}+ C_{pa}+ C_{dd}+ C_{ml})}{f_{\text{ calib}}\cdot \left\langle  \omega'_{p}(\vec{r})\times M (\vec{r}) \right\rangle(1 + B_{q} + B_{k})}.
$$

Blinding the data is important to minimize unconscious biases. This is represented by the clock-blinding factor $f_{\text{ clock}}$. $\omega^{m}_{a}$ is the measured precession frequency, and $C_{i}$ are five different correction terms, associated with the spatial and temporal motion of the beam.

The following table shows all the parameters with their corrections and uncertainties:

![[L99-Paper Review.png]]

[[L99-Paper Review.pdf#page=3&rect=313,436,563,672|L99-Paper Review, p.3]]

> [!PDF|note] [[L99-Paper Review.pdf#page=5&selection=8,0,13,17&color=note|L99-Paper Review, p.5]]
> > The calibration procedure is improved for Run-2-3 compared to Run-1
> 

The improvements reduced the uncertainty to a factor of 20 ppb. This was done by increasing the terms used in the multipole expansion of the magnetic field **Mention number of terms**. Other factors affecting the uncertainty include uncertainties from NMR frequency extraction as well as perturbation caused by the retraction of the trolley from the storage region. Both of these added approximately 20 ppb to the uncertainty.

### Anomalous Precession Frequency

The time dependence of the number of positrons from muon decays that are recorded in a storage period is given by an exponential decay function $N (t)$:

$$
\begin{align}
 N (t) & = N_{0}\eta_{N}(t)e^{-t/\gamma \tau_{\mu}}\times \set{  1 +  A \eta_{A}(t)\cos[\omega_{a}^{m}t + \varphi_{0}+ \eta_{\phi}(t)] },
\end{align}
$$

where $N_{0}$ is the normalization, $\gamma \tau_{\mu}$ is the *time-dilated muon lifetime* (taken to be $\approx 64.4\; \mu s$). $A$ is the average weak-decay asymmetry, and $\varphi_{0}$ is the average phase difference between the muon's momentum and its spin difference at the time of injection. All of $N_{0}$, $A$, and $\varphi_{0}$ have time-dependent correction factors $\eta_{i}$ that account for the horizontal and vertical beam oscillations.

While nearly all of the parameters from above have some energy dependence, $N_{0}$ and $A$ are particularly affected by this. The team chose to combine the data in the *statistically optimal way* of weighting each positron by its energy-dependent asymmetry. Whatever that means.

> [!PDF|note] [[L99-Paper Review.pdf#page=3&selection=517,0,534,54&color=note|L99-Paper Review, p.3]]
> > Seven different analysis groups perform independent extractions of $\omega_{a}^{m}$ by a $\chi^{2}$ minimization. Each analysis team adds an independent blind offset to their result in addition to the aforementioned clock blinding. Two groups perform a new asymmetry-weighted ratio method by subdividing the data and constructing a ratio that preserves statistical power whilst reducing sensitivity to slow rate changes

### Systematic Uncertainty

They used a Brownian bridge model, a model describing Brownian motion with the added restriction that the start and end points yield the same value **Citation?**. They used this model for all three runs, but they dramatically increased the magnetic field maps from 14 in run-1 to 69 in run-2/3. This reduced the uncertainty from tracking the field to 10-16 ppb. They also corrected some tracking bias by 3-10 ppb.

Another source of uncertainty is caused by transient magnetic fields, which themselves are caused by the pulsing ESQs, as well as eddy currents in the kickers. These effects both require correction, and both have been significantly improved from Run-1. During Run-1, the transient magnetic fields caused by the ESQ pulsing, known as $B_{q}$, was measured at a limited number of locations around the ring. To improve this, they used the same petroleum jelly NMR probe, but it was now mounted onto a non-conductive, movable device. This allowed them to map the transient fields between the ESQ plates azimuthally.

Combining this improved mapping with better methodology as well as repeated measurements over time resulted in a reduction of this systematic effect by more than a factor of 4 to 20 ppb.

For the kicker-induced eddy currents, $B_{k}$, the set up was improved to reduce vibrations, which reduced the uncertainty by 3 to 13 ppb

## Statistical Significance

> [!PDF|note] [[L99-Paper Review.pdf#page=6&selection=262,59,286,12&color=note|L99-Paper Review, p.6]]
> > While a comparison between the Fermilab result from Run-1/2/3 presented here, $a_{\mu}$(FNAL), and the 2020 prediction yields a discrepancy of 5.0σ, an updated prediction considering all available data will likely yield a smaller and less significant discrepancy.