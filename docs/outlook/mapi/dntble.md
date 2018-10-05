---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391947"
---
# <a name="dntble"></a>DNTBLE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le téléchargement du contenu d’un dossier à partir du serveur au cours de l' [état de la table du téléchargement](download-table-state.md). Ce processus de téléchargement utilise la synchronisation modification incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Members

 _cEntNew_
  
> [out] Nombre d’éléments ajoutés dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
 _cEntMod_
  
> [out] Nombre d’éléments modifiés sur le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
 _cEntRead_
  
> [out] Nombre d’éléments de lire ou marqués comme non lu dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
 _cEntDel_
  
> [out] Nombre d’éléments supprimés dans le magasin local. Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.
    
## <a name="see-also"></a>Voir aussi



[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

