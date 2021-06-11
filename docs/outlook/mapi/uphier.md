---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414920"
---
# <a name="uphier"></a>UPHIER
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour la synchronisation d’une hiérarchie de dossiers pendant [l’état de la hiérarchie de téléchargement.](upload-hierarchy-state.md)
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> [in] Indicateurs pour modifier le comportement lors de la synchronisation de la hiérarchie de dossiers.
    
  - UPH_OK
    
    - [in] Télécharger a réussi. Le client définit cette information après avoir chargé les informations sur le serveur. Lorsque vous voyez cet indicateur, Outlook effacer toutes les informations de comptabilité internes qui signalaient la hiérarchie de dossiers à mettre à jour. 
    
    - Le client transmet le HRESULT si le chargement n’a pas réussi.
    
_pstmReserved_
  
> [out] Ce membre est réservé à un Outlook interne et n’est pas pris en charge.
    
_iEnt_
  
> [out] Index pour suivre la synchronisation du nombre de dossiers spécifié par  *cEnt*  . 
    
_cEnt_
  
> [out] Nombre de dossiers non synchronisés.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

