---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
ms.openlocfilehash: 90c9338a6b4814bfcb0080109ec070ed0f2c157c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371183"
---
# <a name="uptbl"></a>UPTBL

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le chargement du contenu d’un dossier pendant [l’état de la table de chargement](upload-table-state.md).
  
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
  
> [in] Indicateurs pour déterminer le comportement approprié pendant le chargement.
    
  - UPT_OK
    
    - [in] Télécharger a réussi. Le client le définit après avoir chargé le contenu du dossier sur le serveur.
    
_pstmReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
> [sortant] Nom du dossier.
    
_feid_
  
> [sortant] ID d’entrée du dossier.
    
_uintReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_rgte_
  
> [out] Structure qui contient les informations suivantes pour les éléments normaux (ou non masqués) et les éléments associés (ou masqués) dans le dossier :  _rgte[0]_ est pour les éléments normaux et  _rgte[1]_ pour les éléments associés. 
    
   - nombre d’éléments nouveaux ou modifiés ;
   - nombre d’éléments lus ; 
   - nombre d’éléments supprimés ;
    
 _iEnt_
  
> [out] Index pour suivre le téléchargement du nombre de modifications spécifié par  _cEnt_.
    
_cEnt_
  
> [out] Nombre de modifications apportées au dossier.
    
_movHead_
  
> [out] Chaîne de structures [UPMOV](upmov.md) . 
    
_pReserved_
  
> [sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

