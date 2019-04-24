---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338856"
---
# <a name="uptbl"></a>UPTBL

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le téléchargement du contenu d'un dossier lors de l' [État](upload-table-state.md)de la table de chargement.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
> dans Indicateurs permettant de déterminer le comportement approprié pendant le chargement.
    
  - UPT_OK
    
    - dans Le chargement a réussi. Le client définit cette valeur après avoir téléchargé le contenu du dossier sur le serveur.
    
_pstmReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
> [sortant] Nom du dossier.
    
_feid_
  
> [sortant] ID d’entrée du dossier.
    
_uintReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_rgte_
  
> remarquer Structure pour contenir les informations suivantes pour les éléments normaux (ou non masqués) et les éléments associés (ou masqués) dans le dossier: _rgte [0]_ correspond aux éléments normaux et _rgte [1]_ correspond aux éléments associés. 
    
   - nombre d'éléments nouveaux ou modifiés
   - nombre d'éléments lus 
   - nombre d'éléments supprimés
    
 _iEnt_
  
> remarquer Index permettant de suivre le téléchargement du nombre de modifications spécifiées par _cEnt_.
    
_Motivé_
  
> remarquer Nombre de modifications apportées au dossier.
    
_pupmovHead_
  
> remarquer Chaîne de structures [UPMOV](upmov.md) . 
    
_Disparition_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

