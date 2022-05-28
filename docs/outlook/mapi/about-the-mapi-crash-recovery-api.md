---
title: À propos de l’API de récupération sur incident MAPI
description: Décrit l’API MAPI Crash Recovery, qui vérifie l’état de la mémoire partagée du fichier Dossiers personnels (PST) ou du fichier dossiers hors connexion (OST) pour vérifier que les données sont dans un état cohérent.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
ms.openlocfilehash: d173e730eed03b006729a3120cc4cf885dd1cfdb
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770249"
---
# <a name="about-the-mapi-crash-recovery-api"></a>À propos de l’API de récupération sur incident MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API MAPI Crash Recovery vérifie l’état de la mémoire partagée du fichier Dossiers personnels (PST) ou du fichier dossiers hors connexion (OST) pour vérifier que les données sont dans un état cohérent. S’il est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données des fichiers PST ou OST ouverts vers le disque et verrouille les PST ou les OST et n’autorise aucun accès en lecture ou en écriture aux données. Cela garantit que les données restent dans un état cohérent jusqu’à ce que le processus soit terminé. En veillant à ce que les PST ou les OST soient dans un état cohérent avant l’arrêt du processus, vous pouvez empêcher Microsoft Outlook 2013 et Microsoft Outlook 2010 d’afficher le message d’erreur suivant et d’éviter les problèmes de performances. 
  
 **Un fichier de données n’a pas fermé correctement la dernière fois qu’il a été utilisé et est en cours de vérification pour les problèmes. Les performances peuvent être affectées pendant la vérification en cours.**
  
Cette API fournit les éléments suivants :
  
Constantes:
  
- [Constantes MAPI](mapi-constants.md)
    
Fonctions :
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Voir aussi



[Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

