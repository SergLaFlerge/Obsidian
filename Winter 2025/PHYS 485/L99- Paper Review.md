# Measurement of the Positive Muon Anomalous Magnetic Moment to 0.20 ppm

This paper is self-explanatory. Physicists at  Fermilab present a new measurement of the positive muon magnetic moment  (defined $a_{\mu}\equiv (g_{\mu-2)/2}$) using data collected from the 2019 and 2020 runs of the $g-2$ experiment. Thanks to better running conditions, a more stable beam, and an improved knowledge of the magnetic field weighted by the muon distribution $\tilde{\omega}'_{p}$ as wells the anomalous precession frequency corrected for beam dynamics, the systematic error was reduced by more than a factor of 2 compared to the 2018 run. This time around, they determined $a_{\mu}= 116\;592\; 057 (25)\times 10^{-11}$ $(0.21)$ppm. They combined this result with the previous 2018 **citation needed** result to obtain $116 \; 592 \; 059 (22)\times 10^{-11}$ $(0.20)$ppm. The world average is now given at $a_{\mu}(\text{exp}) = 116 \; 592 \; 059 (22)\times 10^{-11}$ $(0.19)$ppm, which represents a factor of two improvement in precision.

## Introduction

We care about this because precision measurements of things like the muon magnetic anomaly, henceforth called $a_{\mu}$, provide very good tests for the standard model (SM). This is because $a_{\mu}$ can be predicted with high precision theoretically. Any deviation in the measurements compared to theoretical predictions may point to new physics beyond the SM.

Using data collected in 2019 (Run-2) and 2020 (Run-3), the team at Fermilab produced a new measurement for $a_{\mu}$. Compared to previous measurements (Run-1), there was a four-fold increase in detected positrons thanks to improvements made as mentioned in the abstract. All these factors lead to more than a factor of 2 reduction in systematic uncertainties, which surpassed the experiment's design goal.

Run-1 publications describe the principle of the experiment, as well as giving previous results and experimental details.

### Reading Around the Paper

Need more background on why this measurement is important, as well as a description of what $a_{\mu}$ is. No need to go into more detail on the method until we get to the method section.

## Method

> [!PDF|note] [[L99-Paper Review.pdf#page=2&selection=242,0,267,47&color=note|L99-Paper Review, p.2]]
> > The experiment uses $3.1 GeV/c$ polarized muons produced at the Fermilab Muon Campus **citation needed**. Muons are injected into a $7.112$-m radius storage ring that was moved, and significantly upgraded, from the BNL experiment **citation needed**.

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

> [!PDF|note] [[L99-Paper Review.pdf#page=5&selection=8,0,13,17&color=note|L99-Paper Review, p.5]]
> > The calibration procedure is improved for Run-2=3 compared to Run-1
> 
> Start reading from here next.