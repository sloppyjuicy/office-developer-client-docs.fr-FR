---
title: À propos de l’API de récupération sur incident MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321804"
---
# <a name="about-the-mapi-crash-recovery-api"></a>À propos de l’API de récupération sur incident MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'API de récupération d'urgence MAPI vérifie l'état de la mémoire partagée du fichier de dossiers personnels (PST) ou du fichier de dossiers en mode hors connexion (OST) pour vérifier que les données sont dans un état cohérent. Si elle est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données des fichiers PST ou OSTs ouverts vers le disque et verrouille les fichiers PST ou OSTs et n'autorise pas l'accès aux données en lecture ou en écriture. Cela garantit que les données demeurent dans un état cohérent jusqu'à ce que le processus soit terminé. En vous assurant que les fichiers PST ou OSTs sont dans un état cohérent avant la fin du processus, vous pouvez empêcher Microsoft Outlook 2013 et Microsoft Outlook 2010 d'afficher le message d'erreur suivant et éviter les problèmes de performances. 
  
 **Un fichier de données ne s'est pas fermé correctement lors de sa dernière utilisation et est en cours de vérification des problèmes. Les performances peuvent être affectées lorsque la vérification est en cours.**
  
Cette API fournit les éléments suivants:
  
Constantes
  
- [Constantes MAPI](mapi-constants.md)
    
Fonctions :
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Voir aussi



[Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

