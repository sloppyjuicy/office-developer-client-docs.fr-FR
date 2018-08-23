---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584673"
---
# <a name="synccont"></a>SYNCCONT

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation du contenu des dossiers spécifiées dans un magasin local avec le serveur au cours de la [synchronisation de contenu d’un état](synchronize-contents-state.md). Cela implique simplement le téléchargement, ou une synchronisation complète impliquant un téléchargement, puis sur Télécharger.
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation.
    
  - UPC_OK
    
  - [in] Synchronisation complète ou transfert a réussi. Le client définit après la synchronisation des informations avec le serveur.
    
_iEnt_
  
> [out] Index pour effectuer le suivi de synchroniser le contenu dans le nombre de dossiers spécifiée par _cEnt_.
    
_cEnt_
  
> [out] Nombre de dossiers à répliquer.
    
_pvReserved_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_ptagaReserved_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_psosReserved_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

