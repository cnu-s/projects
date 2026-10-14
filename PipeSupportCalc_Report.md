# Training Calculation

## HS-H537 Pipe Support

| Document information | Details |
|---|---|
| Project | McGuire Unit 2 |
| Support | 2-MCT-HS-H537 |
| Support drawing | 2-MCT-HS-H537, Revision 1A |
| Training task | Pipe support calculation using revised 3,100 lb load |
| Status | Training submission — not for design release or field use |
| Calculation basis | PTB and reference calculation MCC-1206.12-40-2102, Client Revision 3 |

> **Training-use notice:** This document summarizes the checks visible in the supplied reference calculation. It is not an independently validated design calculation, does not replace the controlled calculation or its appendices, and is not approved for construction or field use. The complete support load path has not been verified from the supplied excerpts.

## 1. Purpose and scope

The purpose of this training exercise is to review the HS-H537 support against the revised vertical design load of **3,100 lb (3.1 kip)** specified in the Pre-Task Brief (PTB). The review summarizes the pipe-support assembly, HSS cantilever bending, and HSS-to-W8 weld checks reported in the reference calculation.

This submission is limited to the information provided in the PTB, the Revision 1A support drawing, and the supplied excerpts from the reference calculation. The PTB identifies this as a training exercise, allocates 24 hours, specifies no PE stamp, and notes that the preparer is not qualified for the task. Required training, qualified review, and procedure/document checks remain applicable.

## 2. References

1. Pre-Task Brief, Quality Form 517-GU-001, Revision 26-06, pages 1–2 and Part C.
2. Support drawing 2-MCT-HS-H537, Revision 1A, sheet 1 of 1.
3. Calculation Sheet MCC-1206.12-40-2102, Client Revision 3, *Support/Restraint Calculation for Math Model 2HSC*, S/R 2-MCT-HS-H537 (EC 422276), supplied excerpts.
4. Applicable documents identified by the PTB/reference calculation: AD-EG-ALL-1117, AWI-4-23, MCS-1144, MCS-1196, MCS-1206, MCM 1206.00-1059.001, AISC, and the cited component catalogs.

The controlled revisions and applicability of these documents must be confirmed before using the results for engineering release.

## 3. Design basis and input data

| Parameter | Value / description | Source |
|---|---|---|
| Revised vertical support load, `P` | 3,100 lb = 3.1 kip | PTB; reference calculation |
| Existing hot vertical load | 2,325 lb | Support drawing |
| Existing cold vertical load | 1,739 lb | Support drawing |
| Main support column | W8×24, A36 per drawing | Support drawing |
| Cantilever member | HSS 4×4×1/2 in, ASTM A500 Grade B | Reference calculation |
| HSS modulus of elasticity, `E` | 29,000 ksi | Reference calculation |
| HSS yield strength, `Fy` | 46 ksi | Reference calculation |
| HSS section modulus, `S` | 5.97 in³ | Reference calculation |
| HSS moment of inertia, `I` | 11.9 in⁴ | Reference calculation |
| HSS area, `A` | 6.02 in² | Reference calculation |
| HSS design wall thickness | 0.465 in | Reference calculation |
| Load lever arm, `L` | 14 in from W8×24 column centerline to pipe centerline | Reference calculation |
| Pipe clamp | Fig. 295N double-bolt pipe clamp | Reference calculation |
| Hanger components | Fig. 290-LN eye nut; Fig. 140N threaded rod; Fig. 299N clevis; Fig. 55N welding lug | Reference calculation |
| HSS-to-W8 weld | 1/4 in all-around fillet weld; E70XX electrode | Reference calculation |
| W8×24 flange thickness, `t` | 0.40 in | Reference calculation |
| Baseplate/anchors shown on drawing | Four 1/2 in Hilti KB-TZ2 anchors; 2-1/2 in nominal embedment | Support drawing |

### 3.1 Load interpretation

For this review, 3,100 lb is treated as the total revised vertical support load, not as an additional load applied on top of the existing drawing loads. The reference calculation uses a 3.1 kip vertical force at a 14 in lever arm for the HSS cantilever check.

The supplied excerpts do not show other support reaction components or load combinations. Confirm the applicable piping reactions and governing load combinations against the current controlled procedures and piping analysis.

## 4. Calculation and evaluation

### 4.1 Revised load comparison

Increase over the drawing hot load:

`3,100 − 2,325 = 775 lb`

`3,100 / 2,325 = 1.333` → **33.3% above the hot load**

Increase over the drawing cold load:

`3,100 − 1,739 = 1,361 lb`

`3,100 / 1,739 = 1.782` → **78.2% above the cold load**

### 4.2 Pipe-support assembly

The reference calculation compares the 3,100 lb applied load to catalog allowable vertical loads:

| Component | Allowable load (lb) | Interaction ratio, `P / allowable` |
|---|---:|---:|
| Fig. 295N double-bolt pipe clamp | 3,240 | 3,100 / 3,240 = **0.957** |
| Fig. 290-LN weldless eye nut | 3,770 | 3,100 / 3,770 = **0.822** |
| Fig. 140N threaded rod | 3,770 | 3,100 / 3,770 = **0.822** |
| Fig. 299N forged steel clevis | 3,770 | 3,100 / 3,770 = **0.822** |
| Fig. 55N welding lug | 3,770 | 3,100 / 3,770 = **0.822** |

The clamp governs:

`IRassembly = 3,100 / min(3,240, 3,770, 3,770, 3,770, 3,770) = 0.957 ≈ 0.96`

**Reference result:** `IRassembly < 1.0` — reported **O.K.** The clamp has 140 lb of nominal allowable-load margin. Confirm the exact component models, installation configuration, and current catalog allowables.

### 4.3 HSS cantilever bending

Applied moment at the HSS:

`Mz = P × L = 3.1 kip × 14 in = 43.4 kip-in`

Maximum bending stress:

`fb = Mz / S = 43.4 kip-in / 5.97 in³ = 7.27 ksi`

Allowable bending stress used in the reference:

`Fb,allow = 0.6 × Fy = 0.6 × 46 ksi = 27.6 ksi`

Bending interaction ratio:

`IRbending = fb / Fb,allow = 7.27 / 27.6 = 0.264 ≈ 0.26`

**Reference result:** `IRbending < 1.0` — reported **O.K.**

The reference calculation states that shear is not governing but the supplied excerpt does not show a numeric shear ratio. It also states that vertical deflection was evaluated; the numeric deflection and acceptance limit are not visible in the supplied excerpts and require confirmation in the complete calculation.

### 4.4 HSS-to-W8 weld

The reference checks the all-around 1/4 in fillet weld for combined direct shear and bending:

| Quantity | Reference value |
|---|---:|
| Weld-group length, `Lw` | 14.3 in |
| Weld-group section modulus, `Sw` | 17.4 in³ |
| Weld force per unit length, X direction | 2.49 kip/in |
| Weld force per unit length, Y direction | 0.22 kip/in |
| Combined applied weld force per unit length | 2.50 kip/in |
| Allowable E70XX weld force per unit length | 3.71 kip/in |
| Allowable base-metal force per unit length | 5.76 kip/in |

The governing allowable is the lesser of the weld-metal and base-metal values:

`IRweld = 2.50 / min(3.71, 5.76) = 0.674 ≈ 0.67`

**Reference result:** `IRweld < 1.0` — reported **O.K.**

## 5. Summary of results

| Check | Demand / capacity result | Status in supplied reference |
|---|---:|---|
| Pipe-support assembly | Governing ratio = **0.96** (pipe clamp) | O.K.; least margin of the checks shown |
| HSS cantilever bending | Ratio = **0.26** | O.K. |
| HSS shear | Numeric ratio not shown | Stated non-governing |
| HSS vertical deflection | Numeric result/limit not supplied | Confirmation required |
| HSS-to-W8 weld | Ratio = **0.67** | O.K. |
| Baseplate and anchors | Appendix A analysis results not supplied | Not verified in this review |
| Concrete anchorage and slab | Design inputs/results not supplied | Not verified in this review |
| Required load combinations | Not established by supplied excerpts | Confirm against current procedures/piping analysis |

## 6. Conclusion

For the 3,100 lb vertical load and assumptions shown in the supplied reference calculation, the reported utilization ratios are **0.96 for the pipe-support assembly**, **0.26 for HSS bending**, and **0.67 for the HSS-to-W8 weld**. These listed ratios are below 1.0; the pipe clamp is the governing listed component.

This conclusion applies only to the checks and assumptions visible in the supplied excerpts. The reference calculation identifies baseplate/anchor results in Appendix A, but that appendix and the numeric deflection result were not provided. Therefore, this training review does **not** establish overall support adequacy or authorize design release or field use. Confirm the complete controlled calculation, anchor/baseplate/concrete checks, deflection, applicable load combinations, component ratings, and required qualified review before any engineering use.

## 7. Training review record

| Role | Name | Date | Initials / comments |
|---|---|---|---|
| Trainee / preparer |  |  |  |
| Qualified reviewer / mentor |  |  |  |
