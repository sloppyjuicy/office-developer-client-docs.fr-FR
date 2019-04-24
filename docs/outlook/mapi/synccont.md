---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349573"
---
# <a name="synccont"></a>SYNCCONT

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation du contenu des dossiers spécifiés dans un magasin local avec le serveur lors de l'état de la [synchronisation du contenu](synchronize-contents-state.md). Cela implique le simple téléchargement, ou une synchronisation complète impliquant un chargement, puis un téléchargement.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> dans Indicateurs permettant de déterminer le comportement approprié lors de la synchronisation.
    
  - UPC_OK
    
  - dans Le chargement ou la synchronisation complète a réussi. Le client le définit après avoir synchronisé les informations avec le serveur.
    
_iEnt_
  
> remarquer Index à suivre pour effectuer le suivi de la synchronisation du contenu dans le nombre de dossiers spécifiés par _cEnt_.
    
_Motivé_
  
> remarquer Nombre de dossiers à répliquer.
    
_pvReserved_
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
_ptagaReserved_
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
_psosReserved_
  
> Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

