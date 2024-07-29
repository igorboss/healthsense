# Baasmõiste
Suitsetamine (mõnu-või sõltuvusainete tarvitamine)

## Kirjeldus
Anamneesi võtmise käigus tervishoiutöötaja poolt küsitav küsimus, mis määratleb kas patsient suitsetab või tarvitab mingisuguseid mõnu- või sõltuvusaineid

## Küsimused
Kas patsient suitsetab? Kas patsient tarbib nikotiini sisaldavaid tooteid? Kas patsient tarbib tubakat sisaldavaid tooteid? Kas patsient tarbib tubakavabu tooteid?

## Läbiviijad
- [Õde](page:ode) - küsib suitsetamise või mõnu- või sõltuvusainete tarvitamise kohta anamneesi võtmise käigus
- [Perearst](page:perearst) - küsib suitsetamise või mõnu- või sõltuvusainete tarvitamise kohta anamneesi võtmise käigus
- [Eriarst](page:eriarst) - küsib suitsetamise või mõnu- või sõltuvusainete tarvitamise kohta anamneesi võtmise käigus

## Eeldused
- (Fakt - Patsient arsti/õe vastuvõtul) 
- (Fakt - Anamneesi võtmine) 
Kommentaar: kas tuleks teha eraldi selline sedel?

## Andmemudeli kategooria
[ContSys - Observed condition](page:suitsetamine)
[FHIR - Observation](http://hl7.org/fhir/observation.html)

## Andmemudel
## {.tabset}
### Tekstina
- patsient, kohustuslik
- aeg, kohustuslik, minuti täpsusega
- läbiviija
- tulemus ehk "suitsetamise staatus", kohustuslik, loendist [HsTobaccoUser](vs:hs-tobacco-user)
- kommentaar
### Struktureerituna
{{def:tobacco-use-model}}
### Profiil
{{def:tobacco-use}}

## Seotud mõisted
- Kategooria - [THO - Vital sign](concept:observation-category|vital-signs)
- Suitsetamise staatus
  - Koodisüsteem [HsTobaccoUser](cs:hs-tobacco-user)
  - Loend [HsTobaccoUser](vs:hs-tobacco-user)

## Seos FHIR standardiga
- [**Tobacco use status** profiil](https://ig.kodality.dev/healthsense/StructureDefinition-hs-tobacco-use.html)
- [Andmemudeli transformatsioon FHIR Observaton-iks (FML keeles)](/modeler/transformation-definitions/56/edit)
- [Andmemudeli transformatsioon FHIR Observaton-iks (FML-editori abil)](/modeler/transformation-definitions/86/edit)
![](files/52/tobacco-use-fml-transformation.png)




