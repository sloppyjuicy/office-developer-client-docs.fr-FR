---
title: À propos de l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420261"
---
# <a name="about-the-mapi-crash-recovery-api"></a>À propos de l’API de récupération sur incident MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API MAPI Crash Recovery vérifie l’état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST) pour vérifier que les données sont dans un état cohérent. Si elle est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données des PST ou des osts ouverts vers le disque, verrouille les PST ou les osts et n’autorise pas l’accès en lecture ou en écriture aux données. Cela garantit que les données restent dans un état cohérent jusqu’à ce que le processus soit terminé. En vous assurant que les PST ou les systèmes d’exploitation sont dans un état cohérent avant la fin du processus, vous pouvez empêcher Microsoft Outlook 2013 et Microsoft Outlook 2010 d’afficher le message d’erreur suivant et d’éviter les problèmes de performances. 
  
 **Un fichier de données n’a pas été fermé correctement la dernière fois qu’il a été utilisé et des problèmes ont été vérifiés. Les performances peuvent être affectées pendant la vérification.**
  
Cette API fournit les informations suivantes :
  
Constantes :
  
- [Constantes MAPI](mapi-constants.md)
    
Fonctions :
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Voir aussi



[Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

