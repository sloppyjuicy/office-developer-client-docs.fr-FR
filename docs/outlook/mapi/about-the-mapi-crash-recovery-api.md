---
title: À propos de la récupération de panne MAPI API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 34589860ed25f8236a343e16679c2e7a6bdd1e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782860"
---
# <a name="about-the-mapi-crash-recovery-api"></a>À propos de la récupération de panne MAPI API

  
  
**S’applique à**: Outlook 
  
L’API de récupération de panne MAPI vérifie que l’état du fichier de dossiers personnels (PST) ou le fichier de dossiers en mode hors connexion (OST) de la mémoire pour vérifier que les données sont dans un état cohérent partagée. Si elle est dans un état cohérent, la fonction [MAPICrashRecovery](mapicrashrecovery.md) déplace les données de l’ouvrir fichiers pst ou ost sur le disque et verrouille les fichiers pst ou ost et n’autorise pas l’accès en écriture aux données ni lecture. Cela garantit que les données demeurent dans un état cohérent jusqu'à ce que le processus est terminé. En s’assurant que les fichiers pst ou ost est dans un état cohérent avant que le processus est terminé, vous pouvez empêcher l’affichage du message d’erreur suivant Microsoft Outlook 2013 et Microsoft Outlook 2010 et éviter les problèmes de performances. 
  
 **Un fichier de données ne pas fermer correctement la dernière fois qu’il a été utilisé et est en cours d’archivage pour les problèmes. Performances peuvent être affectées alors que la case à cocher est en cours.**
  
Cette API fournit les fonctionnalités suivantes :
  
Constantes :
  
- [Constantes MAPI](mapi-constants.md)
    
Fonctions :
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Voir aussi



[Utiliser l’API de récupération sur incident MAPI](how-to-use-the-mapi-crash-recovery-api.md)

