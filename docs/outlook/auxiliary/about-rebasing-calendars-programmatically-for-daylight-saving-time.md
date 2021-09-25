---
title: À propos du changement de base des calendriers par programme pour l’heure d’été
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 38b342d9-ab10-04b6-5490-9a45f847a60f
description: Dans cette rubrique, cette période entre le ressort et l’automne est appelée période d’été.
ms.openlocfilehash: fba3238543630d3960e41abae427a9757c387639
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614471"
---
# <a name="about-rebasing-calendars-programmatically-for-daylight-saving-time"></a>À propos du changement de base des calendriers par programme pour l’heure d’été

De nombreux pays observent l’heure d’été en avançant les horloges de sorte que les soirs ont plus d’été. Pour ce faire, il faut généralement définir l’horloge avec une heure d’avance au printemps et l’horloge à une heure à l’automne. Dans cette rubrique, cette période entre le ressort et l’automne est appelée période d’été. La plupart des pays ont leurs propres réglementations pour le démarrage et la fin de l’été. Les dates de la période d’heure d’été peuvent changer d’une année à l’autre, et les utilisateurs doivent mettre à jour leur calendrier microsoft Outlook chaque fois que les réglementations de l’heure d’été changent. 
  
Si vous utilisez une version de Windows qui est Windows Vista ou version ultérieure, ou si la mise à jour automatique Windows est désactivée, il se peut que vous ne soyez pas affecté par la modification de l’heure d’été. Sinon, vous devez installer les mises à jour d’été pour Windows. Que les mises à jour soient installées automatiquement, en votre nom par un service informatique ou par vous-même en tant qu’utilisateur personnel, certains rendez-vous existants qui se produisent pendant la période d’heure d’été peuvent afficher des heures incorrectes après l’installation des mises à jour d’heure d’été pour Windows. Cela est vrai pour les rendez-vous périodiques et à instance unique. Vous devez mettre à jour ces rendez-vous pour les afficher correctement dans Outlook, Outlook Web App et dans les applications basées sur CDO (Collaboration Data Objects). La mise à jour incorrecte des rendez-vous affichés sur les calendriers en raison de l’été est appelée rebasing de calendriers.
  
Outlook fournit des outils pour les utilisateurs et Exchange Server des outils permettant aux administrateurs de rebaser les calendriers. Outlook fournit l’outil de mise à jour des données de fuseau horaire pour Outlook utilisateurs. Avec cet outil, les utilisateurs peuvent mettre à jour leurs propres calendriers. Exchange Server fournit l’outil de mise à jour du calendrier Exchange qui permet aux administrateurs d’éviter les difficultés résultant du déploiement large de l’outil Outlook pour tous les utilisateurs et de s’assurer que chaque utilisateur exécute l’outil Outlook correctement.
  
En plus de compter sur les utilisateurs pour exécuter l’outil de mise à jour des données de fuseau horaire ou les administrateurs pour exécuter l’outil de mise à jour du calendrier Exchange, les développeurs de logiciels clients MAPI tiers peuvent télécharger une DLL, Tzmovelib.dll. À l’aide de cet assembly, les développeurs peuvent utiliser les mêmes API que Outlook et Exchange Server dans leurs outils de rebasing de calendrier. 

La liste suivante présente les API de rebasing de calendrier :
  
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
    
Pour écrire un outil de rebasing de rendez-vous à l’aide des API de rebasing de calendrier, vous pouvez utiliser la procédure suivante :
  
1. Utilisez **IOlkApptRebaser::BeginEnumerateAppointments** et **IOlkApptRebaser::EndEnumerateAppointments** pour rechercher les rendez-vous candidats au rebasing. Si nécessaire, présentez des informations pour permettre à l’utilisateur de choisir les rendez-vous à rebaser. Vous pouvez également utiliser MAPI ou le modèle objet Outlook pour examiner les informations d’heure et de périodisation d’un rendez-vous en analyseant les propriétés **PidLidAppointmentTimeZoneDefinitionStartDisplay**, **PidLidAppointmentTimeZoneDefinitionEndDisplay** et **PidLidAppointmentTimeZoneDefinitionRecur.** 
    
2. Utilisez **HrCreateApptRebaser**, **IOlkApptRebaser::BeginRebaseAppointments** et **IOlkApptRebaser::EndRebaseAppointments** pour rebaser le rendez-vous. 
    
Pour obtenir l’assembly Tzmovelib.dll, téléchargez le programme d’installation redistribuable OutlookTimeZoneMoveLibRedist.exe et le fichier d’en-tête Tzmovelib.h à [l’Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b). Ce téléchargement fonctionne pour Outlook 2010 et les versions ultérieures de Outlook. OutlookTimeZoneMoveLibRedist.exe installe le fichier Tzmovelib.dll assembly dans C:\Program Files\MsExTmz. Notez que les applications de rebasing de calendrier tierces peuvent redistribuer uniquement le programme d’installation, les OutlookTimeZoneMoveLibRedist.exe et ne doivent pas redistribuer l’assembly, Tzmovelib.dll ou tout autre composant extrait séparément du programme d’installation.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)
- [Centre d’aide et de support pour l’heure d’été](https://support.microsoft.com/gp/cp_dst)
- [Comment résoudre l’heure d’été à l’aide de l Exchange de mise à jour du calendrier](https://support.microsoft.com/kb/941018)
- [Comment résoudre les changements de fuseau horaire à l’aide de l’outil de mise à jour des données de fuseau horaire pour Microsoft Office Outlook](https://support.microsoft.com/kb/931667)

