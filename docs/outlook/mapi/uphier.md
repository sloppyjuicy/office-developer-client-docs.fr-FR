---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 041ae867ff3a9cc9636ff1d93f9360576e455420
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787424"
---
# <a name="uphier"></a>UPHIER
 
**S’applique à**: Outlook 
  
Informations pour la synchronisation d’une hiérarchie de dossiers au cours de l' [état de la hiérarchie de télécharger](upload-hierarchy-state.md).
  
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
    
    - [in] Téléchargement a réussi. Le client définit après avoir téléchargé correctement les informations sur le serveur. À l’affichage de cet indicateur, Outlook efface toutes les informations de référence interne qui indique la hiérarchie de dossiers nécessaire de mettre à jour. 
    
    - Le client transmet le HRESULT si le transfert n’a pas réussi.
    
_pstmReserved_
  
> [out] Ce membre est réservé à un usage interne Outlook et n’est pas pris en charge.
    
_iEnt_
  
> [out] Index pour effectuer le suivi de la synchronisation du nombre de dossiers spécifiée par *cEnt* . 
    
_cEnt_
  
> [out] Nombre de dossiers qui ne sont pas synchronisés.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

