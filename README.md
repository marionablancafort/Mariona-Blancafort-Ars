# Mariona-Blancafort-Ars
Aquest projecte de Treball de Fi de Grau forma part de l’estudi sobre l'impacte del cicle menstrual en el control glucèmic de dones amb diabetis mellitus tipus 1 (DM1). S’ha desenvolupat un sistema de simulació capaç d’integrar la variabilitat de la sensibilitat a la insulina segons les diferents fases hormonals del cicle menstrual, així com un ajust terapèutic adaptatiu per millorar el control glucèmic dins d’un entorn virtual.


# Estructura del repositori
Aquest repositori inclou exclusivament les dues principals modificacions realitzades sobre el simulador original, desenvolupat per Estremera et al. en l’article “A simulator with realistic and challenging scenarios for virtual T1D patients undergoing CSII and MDI therapy” (2022). Degut a la confidencialitat i restriccions de difusió del codi complet del simulador, no s’inclou la totalitat del projecte, sinó únicament els fitxers propis del present Treball de Fi de Grau, que contenen les funcionalitats desenvolupades.

Els fitxers inclosos són:

- insulin_sensitivity_variability.m:
Funció que genera un perfil cíclic de sensibilitat a la insulina (SI) en funció de les cinc fases del cicle menstrual. Aquesta variabilitat es calcula a partir de dades reals de pacients i s’integra dinàmicament en el simulador per reproduir l’impacte hormonal mensual en el control glucèmic.

- init_mycontroller.m:
Script que defineix els paràmetres de control individualitzats per a cada pacient virtual. Incorpora un algorisme d’ajust terapèutic personalitzat, que modifica els valors de CR, CF i insulina basal segons la fase del cicle i el perfil glucèmic (hipoglucèmia o hiperglucèmia) del pacient.


docs/: Una còpia de l’article científic original del simulador emprat (Estremera et al., 2022) per contextualitzar-ne l’origen i el funcionament base.

results/: Conté els resultats de les simulacions realitzades amb les modificacions implementades. S’hi inclouen fitxers .mat amb les dades simulades i informes AGP (Ambulatory Glucose Profile) generats per a l’anàlisi dels perfils glucèmics.
Degut al gran volum total d’informes generats, només s’hi adjunten alguns exemples representatius per facilitar la consulta i il·lustrar els diferents escenaris simulats.

README.md: Aquest fitxer.


# Requeriments
- Software: MATLAB (preferiblement versió 2020 o superior)
- Toolboxes necessàries: Signal Processing Toolbox i Statistics and Machine Learning Toolbox
- Sistema operatiu: Windows o Linux.

# Execució dels escenaris de simulació

El funcionament del sistema es basa en la modificació del simulador original per analitzar tres escenaris diferenciats. En el primer escenari es manté el simulador sense cap modificació, servint com a base de comparació. En el segon escenari, s’incorpora la variació cíclica de la sensibilitat a la insulina (SI) al llarg del cicle menstrual, però sense aplicar cap ajust terapèutic. Finalment, en el tercer escenari, s’inclou tant la variació de la SI com un algorisme d’ajust de la teràpia insulínica personalitzat, que adapta els paràmetres de dosificació segons la fase del cicle i el perfil glucèmic del pacient. 

Per a cada escenari, es treballa amb una versió diferenciada del simulador, modificant el fitxer principal i els paràmetres del controlador per simular el comportament corresponent. Com que el simulador original és confidencial, en aquest repositori només s’hi ha inclòs la part més rellevant modificada pel present treball, sense poder adjuntar la totalitat del codi.



# Autoria
Mariona Blancafort Ars
Grau en Enginyeria Biomèdica
Universitat de Girona
Curs 2024–2025

Tutor/a: Dr. Josep Vehí Casellas
Projecte realitzat en col·laboració amb: Projecte DIABETEXX i informes MIRA, i el simulador esmentat

