# Daily QA Requirements by Machine Type

> [!info] Why Daily QA Matters  
> Daily Quality Assurance ensures that your linear accelerator delivers precise, consistent radiation doses to patients. These checks detect equipment malfunctions early, maintaining treatment accuracy and patient safety.

## Key Implementation Points

- **Morning Therapist Responsibility:** Daily QA typically performed by trained radiation therapists  
- **Tolerance Levels:** Stricter tolerances for stereotactic procedures (SRS/SBRT)  
- **Documentation:** All results must be documented and reviewed by qualified medical physicist monthly  
- **Action Levels:** Clear procedures needed when tolerances are exceeded

> [!warning] Action Levels When Tolerances Are Exceeded   
> **Level 1:** Investigation required - Continue treatment but monitor closely   
> **Level 2:** Scheduled action within 1-2 days - May continue with mitigation   
> **Level 3:** Immediate action - Stop treatment until problem resolved

> [!note] Clinical Significance   
> The 5% overall dosimetric uncertainty goal (ICRU recommendation) depends on each QA parameter staying within tolerance. Daily checks ensure patient dose accuracy and early detection of equipment drift or malfunction.

## QA Parameters

| QA Parameter                          | Non-IMRT                             | IMRT       | SRS/SBRT   |
| ------------------------------------- | ------------------------------------ | ---------- | ---------- |
| **DOSIMETRY**                         |                                      |            |            |
| X-ray output constancy (all energies) | 3%                                   | 3%         | 3%         |
| Electron output constancy             | Weekly* (Daily if unique monitoring) |            |            |
| **MECHANICAL**                        |                                      |            |            |
| Laser localization                    | 2 mm                                 | 1.5 mm     | 1 mm       |
| Distance indicator (ODI) @ iso        | 2 mm                                 | 2 mm       | 2 mm       |
| Collimator size indicator             | 2 mm                                 | 2 mm       | 1 mm       |
| **SAFETY**                            |                                      |            |            |
| Door interlock (beam off)             | Functional                           | Functional | Functional |
| Door closing safety                   | Functional                           | Functional | Functional |
| Audiovisual monitor(s)                | Functional                           | Functional | Functional |
| Stereotactic interlocks               | N/A                                  | N/A        | Functional |
| Radiation area monitor                | Functional                           | Functional | Functional |
| Beam on indicator                     | Functional                           | Functional | Functional |

## Technical Implementation Details

### Equipment Requirements

- **Dosimetry:** Ion chamber with electrometer (temperature/pressure corrections)  
- **Geometry:** Rulers, calipers, laser alignment tools  
- **Documentation:** Electronic or hardcopy recording system  
- **Backup Systems:** Secondary measurement devices for verification

### Measurement Precision Requirements

- **Repeatability:** 2 standard deviations < tolerance level  
- **Cross-calibration:** Annual comparison with reference standards  
- **Environmental:** Temperature and pressure corrections for ion chambers  
- **Training:** Regular updates for all personnel performing QA


# QA Team Responsibilities

> [!info] QA Team Responsibilities **Qualified Medical Physicist (QMP):**
> 
> - Overall program responsibility and oversight
> - Monthly review and sign-off of all QA records
> - Training and competency assessment
> - Action level determination and protocols
> 
> **Radiation Therapists:**
> 
> - Daily QA test performance
> - Immediate notification of out-of-tolerance results
> - Equipment setup and calibration checks
> - Documentation and record keeping

## Common Issues & Troubleshooting

|Parameter|Common Causes of Deviation|Immediate Actions|
|---|---|---|
|Output Constancy|Temperature/pressure changes, ion chamber drift, beam instability|Check environmental corrections, repeat measurement, verify setup|
|Laser Alignment|Mechanical drift, vibration, thermal expansion|Visual inspection, cross-check with backup system, mechanical adjustment|
|Safety Interlocks|Door adjustment, sensor malfunction, electrical issues|Test all safety systems, contact service engineer immediately|

> [!success] Best Practice Recommendations
> 
> 1. **Standardize Procedures:** Use identical setups and measurement conditions daily
> 2. **Trend Analysis:** Monitor long-term patterns in QA data for early problem detection
> 3. **Backup Systems:** Maintain redundant measurement capabilities
> 4. **Regular Training:** Ensure all staff understand procedures and tolerance requirements
> 5. **Documentation:** Maintain comprehensive records for regulatory compliance


# DAILY QA ESSENTIALS

## TG-142 Recommendations

_Your Daily Dose of Medical Physics Knowledge_

---

> [!tip] WHY DAILY QA MATTERS 
> Daily Quality Assurance is the **first line of defense** in ensuring safe and accurate radiation therapy delivery. These quick checks can detect issues before they impact patient treatment!

---

## DAILY QA CHECKLIST - TG-142

<table> <tr> <th>QA Procedure</th> <th>Non-IMRT</th> <th>IMRT</th> <th>SRS/SBRT</th> </tr> <tr> <td colspan="4" style="background-color: #f0ad4e; font-weight: bold; text-align: center;">DOSIMETRY CHECKS</td> </tr> <tr> <td>☢️ X-ray Output Constancy</td> <td colspan="3" style="text-align: center;">3%</td> </tr> <tr> <td>Electron Output</td> <td colspan="3" style="text-align: center;">Weekly (except machines with unique e monitoring)</td> </tr> <tr> <td colspan="4" style="background-color: #5bc0de; font-weight: bold; text-align: center;">MECHANICAL CHECKS</td> </tr> <tr> <td>🎯 Laser Localization</td> <td>2 mm</td> <td>1.5 mm</td> <td>1 mm</td> </tr> <tr> <td>📏 Distance Indicator (ODI)</td> <td>2 mm</td> <td>2 mm</td> <td>2 mm</td> </tr> <tr> <td>↔️ Collimator Size</td> <td>2 mm</td> <td>2 mm</td> <td>1 mm</td> </tr> <tr> <td colspan="4" style="background-color: #d9534f; font-weight: bold; text-align: center; color: white;">SAFETY CHECKS</td> </tr> <tr> <td>🚪 Door Interlock</td> <td colspan="3" style="text-align: center;">Functional</td> </tr> <tr> <td>⚠️ Door Closing Safety</td> <td colspan="3" style="text-align: center;">Functional</td> </tr> <tr> <td>📹 Audiovisual Monitors</td> <td colspan="3" style="text-align: center;">Functional</td> </tr> <tr> <td>🔺 Stereotactic Interlocks</td> <td>NA</td> <td>NA</td> <td>Functional</td> </tr> <tr> <td>Radiation Monitor</td> <td colspan="3" style="text-align: center;">Functional (if used)</td> </tr> <tr> <td>🔴 Beam On Indicator</td> <td colspan="3" style="text-align: center;">Functional</td> </tr> </table>

---

> [!important] KEY TAKEAWAYS 💡 **Key Points to Remember:**
> 
> • **Tighter tolerances** for stereotactic procedures reflect higher precision requirements
> 
> • **Output constancy** is critical - 3% tolerance for all machine types
> 
> • **Safety interlocks** must be functional every single day
> 
> • **Laser alignment** accuracy varies by treatment type