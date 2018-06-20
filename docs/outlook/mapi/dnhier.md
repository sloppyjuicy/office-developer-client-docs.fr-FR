---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783214"
---
# <a name="dnhier"></a>DNHIER

**S’applique à**: Outlook 
  
Informations pour le téléchargement une hiérarchie à partir du serveur au cours de l' [état de la hiérarchie du téléchargement](download-hierarchy-state.md), qui fait partie d’une synchronisation complète de hiérarchie. Ce processus de téléchargement utilise la synchronisation modification incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Membres

_ulFlags_
  
>  [in] Indicateurs pour déterminer le comportement approprié lors du téléchargement. 
    
   - DNH_OK
    
   - [in] Téléchargement a réussi. Le client définit après le téléchargement des informations à partir du serveur.
    
_pstmReserved_
  
> [out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge. 
    
_pxihc_
  
>  [out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie. Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Nombre de dossiers ajoutés dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
_cEntMod_
  
> [out] Nombre de dossiers à modifier dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
_cEntDel_
  
> [out] Nombre de dossiers à supprimer dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
## <a name="see-also"></a>Voir aussi

- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md) 
- [Constantes MAPI](mapi-constants.md)

