# Main term
Smoking (use of recreational or addictive substances)

## Description
A question asked by a healthcare professional during the medical history taking, which determines whether the patient smokes or uses any kind of recreational or addictive substances

## Questions
Does the patient smoke? Does the patient consume products containing nicotine? Does the patient consume products containing tobacco? Does the patient consume tobacco-free products?

## Actors
- [Nurse](page:nurse) - asks about smoking or the use of tobacco or addictive substances during the taking of medical history.
- [General practitioner](page:general-practitioner) - asks about smoking or the use of tobacco or addictive substances during the taking of medical history.
- [Special care doctor](page:special-care-doctor) - asks about smoking or the use of tobacco or addictive substances during the taking of medical history.

## Prerequisites
- (Fact - Encounter of patient) 
- (Fact - Taking of medical history) 

## Datamodel
## {.tabset}
### Narrative
- patient
- effectiveTime
- actor
- value or "tobacco use status"
- note

### Model
```fsh
Logical: TobaccoUseModel
Parent: Element
* patient 1..1 string "Patient code" "Subject of procedure." 
* effectiveTime 1..1 dateTime "Effective time" "When the observation was measured." 
* actor 1..1 string "Actor code" "Performer of procedure." 
* value 1..1 code "The actual coded result of observation." "" 
* value from https://ig.kodality.dev/healthsense/ValueSet-hs-tobacco-user.json (required) 
* note 0..1 string "Comments about the observation" "Comments about the observation or the results."

Mapping: category 
Id: category 
Title: "Observation category" 
Source: TobaccoUseModel 
Target: "http://terminology.hl7.org/CodeSystem/observation-category" 
* . -> "vital-signs" 

Mapping: sct
Id: sct 
Title: "Value binding to SNOMED CT" 
Source: TobaccoUseModel 
Target: "http://snomed.info/conceptdomain" 
* . -> "229819007 |Tobacco use and exposure|" 
* value -> "702979003 |Never used tobacco| or 702975009 |Ex-tobacco user| or 77176002 |Smoker| or 160603005 |Light cigarette smoker (1-9/day)| or 160604004 |Moderate cigarette smoker (10-19/day)| or 160605003 |Heavy cigarette smoker (20-39/day)| or 160606002 |Very heavy cigarette smoker (40+/day)| or 230065006 |Chain smoker| or 713914004 |User of smokeless tobacco| or 228504007 |User of moist powdered tobacco| or 228494002 |Snuff user| or 81703003 |Chews tobacco| or 228517005 |Chews fine cut tobacco| or 228516001 |Chews loose leaf tobacco| or 228514003 |Chews plug tobacco| or 228518000 |Chews products containing tobacco|"
``` 

### Profile
{{def:tobacco-use}}


## Categories of models
[ContSys - Observed condition](cs:contsys)
[FHIR - Observation](http://hl7.org/fhir/observation.html)

## Related terminology
- Category - [THO - Vital sign](concept:observation-category|vital-signs)
- Smoking status
  - Code system [HsTobaccoUser](cs:hs-tobacco-user)
  - Value set [HsTobaccoUser](vs:hs-tobacco-user)

## Relation with FHIR
- [**Tobacco use status** profile](https://ig.kodality.dev/healthsense/StructureDefinition-hs-tobacco-use.html)
- [**Transformation** of data model to FHIR Observaton](/modeler/transformation-definitions/56/edit)
- [Datamodel transformation to FHIR Observaton (with FML-editor)](/modeler/transformation-definitions/86/edit)
![](files/52/tobacco-use-fml-transformation.png)


