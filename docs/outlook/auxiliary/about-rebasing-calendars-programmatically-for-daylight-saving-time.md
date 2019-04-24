---
title: À propos du changement de base des calendriers par programme pour l’heure d’été
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Dans cette rubrique, cette période entre le printemps et le fléchissement est appelée période d'heure d'été.
ms.openlocfilehash: 8d9a0ffda89ee9d8847cde59181747588a50e947
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316953"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>À propos du changement de base des calendriers par programme pour l’heure d’été

De nombreux pays respectent l'heure d'été en faisant avancer les horloges de manière à ce que les soirs bénéficient d'une date d'été plus longue. Cette opération est généralement réalisée en définissant l'horloge une heure à l'avant dans le ressort et en redéfinissant l'horloge une heure dans l'automne. Dans cette rubrique, cette période entre le printemps et le fléchissement est appelée période d'heure d'été. La plupart des pays ont leurs propres réglementations quant à la date de début et de fin de l'heure d'été. Les dates de la période d'heure d'été peuvent changer de l'année en années, et les utilisateurs doivent mettre à jour leur calendrier Microsoft Outlook chaque fois que les réglementations DST changent. 
  
Si vous utilisez une version de Windows Vista ou version ultérieure, ou si la mise à jour automatique de Windows est activée, vous n'êtes peut-être pas affecté par la modification de l'heure d'été. Dans le cas contraire, vous devez installer les mises à jour de l'heure d'été pour Windows. Que les mises à jour soient installées automatiquement, en votre nom par un service informatique ou par vous-même en tant qu'utilisateur à domicile, certains rendez-vous existants pendant la période d'heure d'été peuvent afficher des temps incorrects après l'installation des mises à jour de l'heure d'été pour Windows. . Ceci est vrai pour les rendez-vous périodiques et uniques. Vous devez mettre à jour ces rendez-vous pour qu'ils s'affichent correctement dans Outlook Web App et dans les applications basées sur CDO (Collaboration Data Objects). La mise à jour des rendez-vous affichés de manière incorrecte sur des calendriers en raison de la relocalisation des calendriers.
  
Outlook fournit des outils pour les utilisateurs et Exchange Server fournit aux administrateurs des outils permettant de rebaser les calendriers. Outlook fournit l'outil de mise à jour des données de fuseau horaire pour les utilisateurs d'Outlook. Grâce à cet outil, les utilisateurs peuvent mettre à jour leurs propres calendriers. Exchange Server fournit l'outil de mise à jour de calendrier Exchange qui aide les administrateurs à éviter les difficultés résultant du déploiement de l'outil Outlook de manière étendue pour tous les utilisateurs et pour s'assurer que chaque utilisateur exécute correctement l'outil Outlook.
  
En plus de faire en sorte que les utilisateurs puissent exécuter l'outil de mise à jour des données de fuseau horaire ou les administrateurs pour exécuter l'outil de mise à jour de calendrier Exchange, les développeurs de logiciels clients MAPI tiers peuvent télécharger un fichier DLL, Tzmovelib. dll. À l'aide de cet assembly, les développeurs peuvent utiliser les mêmes API que celles d'Outlook et d'Exchange Server dans leurs outils de relocalisation de calendrier. 

La liste suivante présente les API de relocalisation du calendrier:
  
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
    
Pour écrire un outil de relocalisation de rendez-vous à l'aide des API de relocalisation du calendrier, vous pouvez utiliser la procédure suivante:
  
1. Utilisez **IOlkApptRebaser:: BeginEnumerateAppointments** et **IOlkApptRebaser:: EndEnumerateAppointments** pour rechercher les rendez-vous qui sont candidats à la relocalisation. Si nécessaire, présentez les informations pour permettre à l'utilisateur de décider des rendez-vous à relocaliser. Vous pouvez également utiliser MAPI ou le modèle objet Outlook pour examiner les informations de temps et de récurrence d'un rendez-vous en analysant **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, et les propriétés **PidLidAppointmentTimeZoneDefinitionRecur** . 
    
2. Utilisez **HrCreateApptRebaser**, **IOlkApptRebaser:: BeginRebaseAppointments**et **IOlkApptRebaser:: EndRebaseAppointments** pour rebaser le rendez-vous. 
    
Pour obtenir l'assembly Tzmovelib. dll, téléchargez le programme d'installation redistribuable de OutlookTimeZoneMoveLibRedist. exe et le fichier d'en-tête Tzmovelib. h sur [Outlook 2010: fichier d'en-tête et programme d'installation redistribuable de référence auxiliaire pour les calendriers de](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) relocalisation . Ce téléchargement fonctionne pour Outlook 2010 et les versions ultérieures d'Outlook. OutlookTimeZoneMoveLibRedist. exe installe le fichier d'assembly Tzmovelib. dll dans C:\Program Files\MsExTmz. Notez que les applications de relocalisation de calendrier tierces ne peuvent redistribuer que le programme d'installation, OutlookTimeZoneMoveLibRedist. exe, et ne doivent pas redistribuer l'assembly, Tzmovelib. dll ou tout autre composant extrait séparément du programme d'installation.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centre d'aide et de support pour l'heure d'été](https://support.microsoft.com/gp/cp_dst)
- [Comment corriger l'heure d'été à l'aide de l'outil de mise à jour de calendrier Exchange](https://support.microsoft.com/kb/941018)
- [Comment résoudre les changements de fuseau horaire à l'aide de l'outil de mise à jour des données de fuseau horaire pour Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

