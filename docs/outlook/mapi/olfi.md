---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
ms.openlocfilehash: 82d2c144db85b73a3409b2cfca86a13841d076eb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376132"
---
# <a name="olfi"></a>OLFI

**S’applique à** : Outlook 2013 | Outlook 2016
  
File d’attente des structures d’ID à long terme utilisées par le fournisseur de magasins de dossiers personnels (PST) pour affecter un ID d’entrée pour un nouveau message ou dossier en mode hors connexion.
  
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
  
- Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.

 _ulReserved_
  
- Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.

 _dwAlloc_
  
- Nombre d’entrées disponibles pour l’allocation. Ces entrées partagent le même identificateur global unique (GUID).

 _dwNextAlloc_
  
- Nombre d’entrées disponibles en plus pour l’allocation. Ces entrées partagent le même GUID.

 _ltidAlloc_
  
- Structure d’ID à long terme, **[LTID](ltid.md)**, identifiant l’entrée actuellement disponible pour l’allocation. La structure d’ID à long terme contient un GUID et un index identifiant un objet dans le magasin. Ensemble, le GUID et l’index peuvent former un ID d’entrée unique pour un objet.

 _ltidNextAlloc_
  
- Structure d’ID à long terme identifiant l’entrée disponible suivante.

## <a name="remarks"></a>Remarques

Un ID d’entrée est un identificateur d’entrée MAPI de 4 byte pour un dossier ou un message. Pour plus d’informations, voir [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Lorsqu’un fournisseur de magasin PST affecte un ID d’entrée à un nouvel objet, il a d’abord besoin d’un GUID qui identifie le serveur et d’un index qui identifie l’objet dans le magasin. Même si le GUID n’est pas unique sur tous les ID d’entrée, le GUID et l’index combinés fournissent une entrée unique. Cette paire GUID et index est suivi par une structure d’ID à long terme, **LTID**, qui fait partie de la structure **OLFI** .
  
Le fournisseur de magasins PST ne conserve pas physiquement dans **OLFI** une structure **LTID** pour chaque paire GUID-index. Il conserve une structure **LTID** , _ltidAlloc_, pour la première paire GUID-index actuellement disponible ; nombre, _dwAlloc_, du nombre d’entrées disponibles qui partagent ce même GUID ; et une deuxième structure **LTID** , _ltidNextAlloc_, pour la paire GUID-index disponible suivante qui a un GUID différent. Le fournisseur de magasins PST utilise la structure **OLFI** pour suivre les GUID et les index qu’il a distribués. À un niveau virtuel, le fournisseur conserve une réserve d’un certain nombre de structures **LTID** prêtes à être allouées. _dwAlloc tient_ à jour le nombre de structures **LTID** disponibles.
  
Les demandes d’ID d’entrée sont des blocs. Lorsqu’une demande de bloc est demandée, le fournisseur de magasins PST vérifie si la réserve est suffisante en comparant la taille demandée à _dwAlloc_. S’il existe une réserve suffisante, elle renvoie le GUID et l’index _dans ltidAlloc_ pour l’allocation. Il diminue ensuite _dwAlloc_ par la taille demandée et incrémente l’index en _ltidAlloc_ par la taille demandée. Cela prépare le fournisseur de magasin PST à allouer _ltidAlloc_ à la demande suivante pour un autre bloc d’ID d’entrée. Notez que le GUID reste le même pour la requête suivante.
  
Si la taille d’une demande est supérieure à _dwAlloc_, le fournisseur de magasins PST tente d’utiliser ce qu’il a en réserve, comme spécifié par _dwNextAlloc_ et _ltidNextAlloc_. Il copie _dwNextAlloc_ et _ltidNextAlloc_ vers _dwAlloc_ et _ltidAlloc_ respectivement, et définit _dwNextAlloc_ et _ltidNextAlloc_ sur NULL.
  
Un fournisseur qui encapsule le fournisseur de magasin PST doit régulièrement vérifier _ltidNextAlloc_ pour voir s’il est NULL. Si c’est le cas, le fournisseur doit le remplir avec un nouveau GUID et réinitialiser _dwNextAlloc_ afin d’allouer davantage d’ID d’entrée.
  
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)
 [À propos de la machine à états de réplication](about-the-replication-state-machine.md)
 [LTID](ltid.md)
