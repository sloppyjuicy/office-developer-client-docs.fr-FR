---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279752"
---
# <a name="olfi"></a>OLFI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
File d'attente des structures d'ID à long terme utilisées par le fournisseur de magasins de fichiers de dossiers personnels (PST) pour affecter un ID d'entrée pour un nouveau message ou dossier en mode hors connexion.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>Membres

 _ulVersion_
  
- Numéro de version de la structure. 
    
 _muidReserved_
  
- Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.
    
 _ulReserved_
  
- Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.
    
 _dwAlloc_
  
- Nombre d'entrées pouvant être allouées. Ces entrées partagent le même GUID (globally unique identifier).
    
 _dwNextAlloc_
  
- Nombre d'entrées disponibles à la suite de l'allocation. Ces entrées partagent le même GUID.
    
 _ltidAlloc_
  
- La structure de l'ID à long terme, **[LTID](ltid.md)**, qui identifie l'entrée actuellement disponible pour l'allocation. La structure de l'ID à long terme contient un GUID et un index identifiant un objet dans le magasin. Ensemble, le GUID et l'index peuvent former un ID d'entrée unique pour un objet. 
    
 _ltidNextAlloc_
  
- Structure de l'ID à long terme identifiant la prochaine entrée disponible.
    
## <a name="remarks"></a>Remarques

Un ID d'entrée est un identificateur d'entrée MAPI de 4 octets pour un dossier ou un message. Pour plus d'informations, consultez la rubrique [EntryID](https://msdn.microsoft.com/library/ms836424).
  
Lorsqu'un fournisseur de banque de fichiers PST affecte un ID d'entrée à un nouvel objet, il a besoin d'un GUID qui identifie le serveur et d'un index qui identifie l'objet dans le magasin. Même si le GUID n'est pas unique pour tous les identificateurs d'entrée, le GUID et l'index combinés fournissent une entrée unique. Ce GUID et cette paire d'index sont suivis par une structure d'ID à long terme, **LTID**, qui fait partie de la structure **OLFI** . 
  
Le fournisseur de banque de fichiers PST ne conserve pas physiquement **OLFI** une structure **LTID** pour chaque paire GUID-index. Il conserve une structure **LTID** , *ltidAlloc* , pour la première paire GUID-index actuellement disponible; nombre, *dwAlloc* , du nombre d'entrées disponibles qui partagent ce même GUID; et une deuxième structure **LTID** , *ltidNextAlloc* , pour la prochaine paire GUID-index disponible dont le GUID est différent. Le fournisseur de banque de fichiers PST utilise la structure **OLFI** pour effectuer le suivi des GUID et des index qu'il a remis. À un niveau virtuel, le fournisseur conserve une réserve d'un certain nombre de structures **LTID** prêtes à être allouées.  *dwAlloc* conserve le décompte des structures **LTID** disponibles. 
  
Les demandes d'ID d'entrée sont des blocs. Lorsqu'il y a une demande pour un bloc, le fournisseur de banque PST vérifie si la réserve est suffisante en comparant la taille demandée à *dwAlloc* . Si la réserve est suffisante, elle renvoie le GUID et l'index dans *ltidAlloc* pour l'allocation. Il réduit ensuite *dwAlloc* de la taille demandée et incrémente l'index de *ltidAlloc* selon la taille demandée. Cette étape permet de préparer le fournisseur de banque d'adresses de dossiers personnels afin d'allouer *ltidAlloc* à la requête suivante pour un autre bloc d'ID d'entrée. Notez que le GUID reste le même pour la requête suivante. 
  
Si la taille d'une requête est supérieure à *dwAlloc* , le fournisseur de banque d'informations PST tente d'utiliser ce dernier en réserve, comme spécifié par *dwNextAlloc* et *ltidNextAlloc* . Il copie *dwNextAlloc* et *ltidNextAlloc* dans *dwAlloc* et *LtidAlloc* respectivement, et définit *dwNextAlloc* et *ltidNextAlloc* sur null. 
  
Un fournisseur qui encapsule le fournisseur de magasin PST doit vérifier régulièrement *ltidNextAlloc* pour voir s'il est null. Si c'est le cas, le fournisseur doit le remplir avec un nouveau GUID et réinitialiser *dwNextAlloc* afin que d'autres ID d'entrée puissent être alloués. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

