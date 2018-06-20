---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787460"
---
# <a name="uptbl"></a>UPTBL

**S’applique à**: Outlook 
  
Informations de téléchargement du contenu d’un dossier pendant la [Télécharger l’état de la table](upload-table-state.md).
  
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
  
> [in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.
    
  - UPT_OK
    
    - [in] Téléchargement a réussi. Le client définit après avoir téléchargé le contenu du dossier sur le serveur.
    
_pstmReserved_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pszName_
  
> [out] Nom du dossier.
    
_feid_
  
> [out] ID d’entrée du dossier.
    
_uintReserved_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_rgte_
  
> [out] Structure contenant les informations suivantes pour les éléments normales (ou non masqués) et associée (ou masqué) dans le dossier : _rgte [0]_ est pour les éléments normales et _rgte [1]_ des éléments associés. 
    
   - le nombre d’éléments nouveaux ou modifiés
   - le nombre d’éléments lus 
   - le nombre d’éléments supprimés
    
 _iEnt_
  
> [out] Index pour effectuer le suivi de téléchargement le nombre de modifications spécifié par _cEnt_.
    
_cEnt_
  
> [out] Nombre de modifications dans le dossier.
    
_pupmovHead_
  
> [out] Chaîne de structures [UPMOV](upmov.md) . 
    
_Conservés_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

