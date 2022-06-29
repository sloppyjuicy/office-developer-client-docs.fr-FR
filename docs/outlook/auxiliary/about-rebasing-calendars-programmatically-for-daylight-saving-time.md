---
title: À propos du changement de base des calendriers par programme pour l’heure d’été
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Dans cette rubrique, cette période entre le printemps et l’automne est appelée période DST.
ms.openlocfilehash: 83d77711df9109323c84d37b18f33ec4cef2fb8c
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448573"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>À propos du changement de base des calendriers par programme pour l’heure d’été

De nombreux pays observent l’heure d’été (DST) en avançant les horloges afin que les soirées aient un jour plus long. Cela est généralement fait en définissant l’horloge une heure à l’avance au printemps, et en définissant l’horloge une heure en arrière à l’automne. Dans cette rubrique, cette période entre le printemps et l’automne est appelée période DST. La plupart des pays ont leurs propres réglementations concernant le démarrage et la fin de l’authentification DST. Les dates de la période DST peuvent changer d’une année à l’autre, et les utilisateurs doivent mettre à jour leur calendrier Microsoft Outlook chaque fois que la réglementation DST change. 
  
Si vous utilisez une version de Windows qui est Windows Vista ou une version ultérieure, ou si la mise à jour automatique de Windows est activée, il se peut que vous ne soyez pas affecté par la modification de l’heure d’été. Sinon, vous devez installer les mises à jour DST pour Windows. Que les mises à jour soient installées automatiquement, en votre nom par un service informatique ou par vous-même en tant qu’utilisateur à domicile, certains rendez-vous existants qui se produisent pendant la période DST peuvent afficher des heures incorrectes après l’installation des mises à jour DST pour Windows. Cela est vrai pour les rendez-vous périodiques et à instance unique. Vous devez mettre à jour ces rendez-vous pour les afficher correctement dans Outlook, Outlook Web App et dans les applications basées sur les objets de données de collaboration (CDO). La mise à jour des rendez-vous affichés incorrectement sur les calendriers en raison de la DST est appelée rebasage des calendriers.
  
Outlook fournit des outils pour les utilisateurs et Exchange Server fournit des outils permettant aux administrateurs de rebaser des calendriers. Outlook fournit l’outil de mise à jour des données de fuseau horaire pour les utilisateurs Outlook. Avec cet outil, les utilisateurs peuvent mettre à jour leurs propres calendriers. Exchange Server fournit l’outil de mise à jour du calendrier Exchange qui permet aux administrateurs d’éviter les difficultés résultant du déploiement de l’outil Outlook largement sur tous les utilisateurs et de s’assurer que chaque utilisateur exécute correctement l’outil Outlook.
  
En plus de s’appuyer sur les utilisateurs pour exécuter l’outil time zone data update ou les administrateurs pour exécuter l’outil de mise à jour du calendrier Exchange, les développeurs de logiciels clients MAPI tiers peuvent télécharger une DLL, Tzmovelib.dll. À l’aide de cet assembly, les développeurs peuvent utiliser les mêmes API qu’Outlook et Exchange Server utiliser dans leurs outils de rebasage de calendrier. 

La liste suivante montre les API de rebasage du calendrier :
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Pour écrire un outil de rebasage de rendez-vous à l’aide des API de rebasage de calendrier, vous pouvez utiliser la procédure suivante :
  
1. Utilisez **IOlkApptRebaser::BeginEnumerateAppointments** et **IOlkApptRebaser::EndEnumerateAppointments** pour rechercher les rendez-vous qui sont candidats au rebasage. Si nécessaire, présentez des informations pour permettre à l’utilisateur de décider quels rendez-vous rebasculer. Vous pouvez également utiliser MAPI ou le modèle objet Outlook pour examiner l’heure et la périodicité d’un rendez-vous en analysant les propriétés **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** et **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Utilisez **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** et **IOlkApptRebaser::EndRebaseAppointments pour rebaser** le rendez-vous. 
    
Pour obtenir l’assembly Tzmovelib.dll, téléchargez le programme d’installation redistribuable OutlookTimeZoneMoveLibRedist.exe et le fichier d’en-tête Tzmovelib.h dans [Outlook 2010 : Programme d’installation redistribuable de référence auxiliaire et fichier d’en-tête pour la rebasation des calendriers](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). Ce téléchargement fonctionne pour Outlook 2010 et versions ultérieures d’Outlook. OutlookTimeZoneMoveLibRedist.exe installe le fichier d’assembly Tzmovelib.dll dans C:\Program Files\MsExTmz. Notez que les applications de rebasage de calendrier tiers peuvent redistribuer uniquement le programme d’installation, OutlookTimeZoneMoveLibRedist.exe et ne doivent pas redistribuer l’assembly, Tzmovelib.dll ou tout autre composant extrait séparément du programme d’installation.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centre d’aide et de support pour l’heure d’été](https://support.microsoft.com/gp/cp_dst)
`- [How to address daylight saving time by using the Exchange Calendar Update Tool](https://support.microsoft.com/kb/941018)`
- [Comment résoudre les modifications de fuseau horaire à l’aide de l’outil time zone data update pour Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

