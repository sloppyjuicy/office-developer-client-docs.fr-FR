---
title: À propos de redéfinir des calendriers par programme à l’heure
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Dans cette rubrique, cette période entre le ressort et la baisse est appelée pour la période d’heure d’été.
ms.openlocfilehash: 4787b2143b3f5d1f0400524f0da82e19e2cbed8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782541"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>À propos de redéfinir des calendriers par programme à l’heure

De nombreux pays observer l’heure (heure d’été) en exécutant les horloges afin que l’heure d’été plu soirée. Cette opération est généralement effectuée en définissant l’horloge avance une heure au printemps et réglage de l’horloge d’une heure retour à l’automne. Dans cette rubrique, cette période entre le ressort et la baisse est appelée pour la période d’heure d’été. La plupart des pays ont leur propre réglementation pour lorsque l’heure d’été commence et se termine. Les dates de la période d’heure d’été peuvent modifier l’année à, et les utilisateurs doivent mettre à jour leur calendrier Microsoft Outlook chaque fois que les règles d’heure d’été modifient. 
  
Si vous utilisez une version de Windows est Windows Vista ou version ultérieure, ou Windows mise à jour automatique est activée, vous ne pouvez pas être affectées par la modification de l’heure d’été. Dans le cas contraire, vous devez installer les mises à jour de l’heure d’été pour Windows. Si les mises à jour sont installés automatiquement à votre place par vous-même ou par un service informatique en tant qu’un utilisateur à domicile, indépendamment de certains rendez-vous existants qui se produisent pendant la période d’heure d’été peuvent afficher des heures incorrectes après l’installent des mises à jour de l’heure d’été pour Windows . Cela est vrai pour les rendez-vous périodiques et uniques. Vous devez mettre à jour ces rendez-vous afin de les afficher correctement dans Outlook, Outlook Web App et dans les applications qui sont basées sur les objets CDO (Collaboration Data). Mise à jour des rendez-vous incorrectement affichés sur les calendriers en raison de l’heure d’été est appelé redéfinir des calendriers.
  
Outlook fournit des outils pour les utilisateurs et Exchange Server fournit des outils pour les administrateurs de calendriers rebase. Outlook fournit l’outil de mise à jour de données de fuseau horaire pour les utilisateurs d’Outlook. Avec cet outil, les utilisateurs peuvent mettre à jour leurs calendriers. Exchange Server fournit l’outil de mise à jour de calendrier Exchange qui permet aux administrateurs pour éviter les problèmes de déploiement de l’outil Outlook largement à tous les utilisateurs et pour vous assurer que chaque utilisateur exécute l’outil Outlook correctement.
  
Outre le recours aux utilisateurs d’exécuter l’outil de mise à jour de données de fuseau horaire ou aux administrateurs d’exécuter l’outil de mise à jour du calendrier Exchange, les développeurs de logiciels tiers MAPI client peuvent télécharger une DLL, Tzmovelib.dll. À l’aide de cet assembly, les développeurs peuvent utiliser les mêmes API Outlook et Exchange Server utilisent dans leur calendrier redéfinition des outils. 

La liste suivante montre la redéfinition des API de calendrier :
  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
    
- [IOlkApptRebaser](iolkapptrebaser.md)
    
- [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)
    
- [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)
    
- [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)
    
- [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)
    
- [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)
    
- [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)
    
- [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)
    
- [RebaseTaskComplete](rebasetaskcomplete.md)
    
- [RebaseTaskProgress](rebasetaskprogress.md)
    
- [TZDEFINITION](tzdefinition.md)
    
- [TZREG](tzreg.md)
    
- [TZRULE](tzrule.md)
    
Pour écrire un outil de redéfinition rendez-vous à l’aide du calendrier de redéfinition des API, vous pouvez utiliser la procédure suivante :
  
1. Utilisez **IOlkApptRebaser::BeginEnumerateAppointments** et **IOlkApptRebaser::EndEnumerateAppointments** pour rechercher les rendez-vous qui sont des candidats pour redéfinir. Si nécessaire, présenter des informations pour permettre à l’utilisateur à décider quels rendez-vous relocaliser. Vous pouvez également utiliser MAPI ou le modèle objet Outlook pour examiner les informations de temps et de périodicité d’un rendez-vous en analysant les **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay**, les propriétés **PidLidAppointmentTimeZoneDefinitionRecur** et. 
    
2. Utilisez **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments**et **IOlkApptRebaser::EndRebaseAppointments** pour redéfinir le rendez-vous. 
    
Pour obtenir l’assembly Tzmovelib.dll, téléchargez le programme d’installation redistribuable OutlookTimeZoneMoveLibRedist.exe et le fichier d’en-tête Tzmovelib.h à [Outlook 2010 : programme d’installation redistribuable auxiliaire référence et fichier d’en-tête pour redéfinir des calendriers](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b) . Ce téléchargement fonctionne pour Outlook 2010 et versions ultérieures d’Outlook. OutlookTimeZoneMoveLibRedist.exe installe le fichier d’assembly Tzmovelib.dll dans C:\Program Files\MsExTmz. Notez que les applications de redéfinition de calendrier tiers peuvent redistribuer uniquement le programme d’installation, OutlookTimeZoneMoveLibRedist.exe et ne doivent pas redistribuer l’assembly, Tzmovelib.dll ou n’importe quelle autre extraites des composants séparément le programme d’installation.
  
## <a name="see-also"></a>Voir aussi

- [À propos de persistance TZDEFINITION dans un flux de valider une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analyser un flux de données à partir d’une propriété binaire à lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analyser un flux de données à partir d’une propriété binaire à lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
- [L’heure d’été Centre d’aide et support technique](http://support.microsoft.com/gp/cp_dst)
- [Comment résoudre l’heure d’été à l’aide de l’outil de mise à jour de calendrier Exchange](http://support.microsoft.com/kb/941018)
- [Comment résoudre les modifications de fuseau horaire à l’aide de l’outil de mise à jour de données de fuseau horaire pour Microsoft Office Outlook](http://support.microsoft.com/kb/931667)

