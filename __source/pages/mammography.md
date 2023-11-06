## Definition
[Mammography](concept:snomed-ct|71651007) (also called mastography) is the process of using low-energy X-rays (usually around 30 kVp) 
to examine the human breast for diagnosis and screening. The goal of mammography is the early detection of [breast cancer](concept:snomed-ct|254837009), 
typically through detection of characteristic masses or [microcalcifications](concept:snomed-ct|12747003).

## Description
As with all X-rays, [mammograms](https://www.cdc.gov/cancer/breast/basic_info/mammograms.htm) use doses of [ionizing radiation](concept:snomed-ct|125576007) to create images. 
These images are then analyzed for abnormal findings. It is usual to employ lower-energy X-rays, 
typically Mo (K-shell X-ray energies of 17.5 and 19.6 keV) and Rh (20.2 and 22.7 keV) than those used for radiography of bones. 
Mammography may be 2D or 3D (tomosynthesis), depending on the available equipment and/or purpose of the examination. 
Ultrasound, ductography, positron emission mammography (PEM), and magnetic resonance imaging ([MRI](page:mri)) are adjuncts to mammography. 
Ultrasound is typically used for further evaluation of masses found on mammography or palpable masses that may or may not be seen on mammograms. 
Ductograms are still used in some institutions for evaluation of bloody nipple discharge when the mammogram is non-diagnostic. 
MRI can be useful for the screening of high risk patients, for further evaluation of questionable findings or symptoms, as well as for pre-surgical evaluation of patients with known breast cancer, 
in order to detect additional lesions that might change the surgical approach (for example, from breast-conserving lumpectomy to mastectomy).

## Informational Model
```fsh
Logical: MammographyModel
Parent: Element
* code           1..1     Coding                        "Code" "Code of the imaging procedure."
* code from https://terminology.kodality.dev/api/fhir/ValueSet/mammography-codes (required)
* patient       1..1     Reference(Patient)    "Patient" "Subject of procedure."
* performer  0..1 Reference(Practitioner or PractitionerRole) "Performer" "The people who performed the procedure."
* performed 1..1 dateTime                    "Effective date and time" "When the procedure was performed."
* device        0..1 Reference(Device) "Used device." ""
//* action         0..1 Coding "Kind of action with device" ""
//* action from https://terminology.kodality.dev/api/fhir/ValueSet/mammography-action (required)
* bodySite    0..1 Coding "Target body site" ""
* bodySite from https://terminology.kodality.dev/api/fhir/ValueSet/mammography-bodysite (required)
* outcome   1..1 Coding "Outcome" "The result of procedure."
* outcome from https://terminology.kodality.dev/api/fhir/ValueSet/mammography-outcome (required)
* note          1..* string "Additional information about the procedure" ""
```

