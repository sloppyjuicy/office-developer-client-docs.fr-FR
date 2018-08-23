---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7d01f07b5eb5ca34b4bd825b62b7d1520b853d6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564261"
---
# <a name="olfi"></a>OLFI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
File d’attente des structures de ID à long terme utilisé par le fournisseur de banque de dossiers personnels (PST) de fichier pour attribuer un ID d’entrée pour un nouveau message ou un dossier en mode hors connexion.
  
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

## <a name="members"></a>Members

 _ulVersion_
  
- Numéro de version de la structure. 
    
 _muidReserved_
  
- Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _ulReserved_
  
- Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _dwAlloc_
  
- Le nombre d’entrées qui sont disponibles pour l’affectation. Ces entrées de partagent le même identificateur global unique (GUID).
    
 _dwNextAlloc_
  
- Le nombre d’entrées qui sont ensuite disponibles pour l’allocation. Ces entrées partagent le même GUID.
    
 _ltidAlloc_
  
- À long terme ID structure, **[LTID](ltid.md)**, qui identifie l’entrée actuellement disponible pour affectation. La structure de code à long terme contient un GUID et un index qui identifie un objet dans le magasin. Le GUID et l’index peuvent forment un identificateur d’entrée unique pour un objet. 
    
 _ltidNextAlloc_
  
- Structure d’ID à long terme qui identifie l’entrée suivante disponible.
    
## <a name="remarks"></a>Remarques

Un ID d’entrée est un identificateur d’entrée MAPI 4 octets pour un dossier ou un message. Pour plus d’informations, voir la [propriété ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).
  
Lorsqu’un fournisseur de magasins PST affecte un ID d’entrée à un nouvel objet, il doit tout d’abord un GUID qui identifie le serveur et un index qui identifie l’objet dans le magasin. Même si le GUID n’est pas unique parmi tous les identificateurs d’entrée, le GUID et l’index combinés fournissent une entrée unique. Cette paire GUID et l’index est suivie par une structure d’ID à long terme, **LTID**, qui fait partie de la structure **OLFI** . 
  
Le fournisseur de banque PST ne pas physiquement conserve dans **OLFI** une structure **LTID** pour chaque paire de GUID-index. Il conserve une structure **LTID** , *ltidAlloc* , pour la paire GUID-index disponible en premier ; un nombre, *dwAlloc* , le nombre d’entrées disponibles qui partagent ce même GUID ; et une deuxième structure **LTID** , *ltidNextAlloc* , pour la paire GUID-index disponible suivante qui a un GUID différent. Le fichier PST stocker fournisseur utilise la structure **OLFI** pour suivre les GUID et les index qu’il a attribuées. Un niveau virtuel, le fournisseur maintient une réserve d’un nombre de structures **LTID** qui sont prêts à être allouée.  *dwAlloc* conserve un décompte des structures **LTID** disponibles. 
  
Les demandes pour les identificateurs d’entrée sont fournis dans les blocs. Lorsqu’il existe une demande pour un bloc, le fournisseur de banque PST vérifie s’il existe suffisamment réserve disponible en comparant la taille demandée avec *dwAlloc* . S’il existe des réserves suffisantes, elle renvoie le GUID et l’index *ltidAlloc* d’attribution. Il diminue *dwAlloc* la taille demandée, puis incrémente la taille requise de l’index de *ltidAlloc* . Il prépare le fournisseur de banque PST à allouer *ltidAlloc* sur la requête suivante pour un autre bloc d’identificateurs d’entrée. Notez que le GUID reste identique pour la requête suivante. 
  
Si la taille d’une requête est supérieure à *dwAlloc* , le fournisseur de banque PST essaie d’utiliser ce que cela a ensuite en réserve, comme spécifié par *dwNextAlloc* et *ltidNextAlloc* . Il copie *dwNextAlloc* et *ltidNextAlloc* *dwAlloc* et *ltidAlloc* et définit *dwNextAlloc* et *ltidNextAlloc* sur NULL. 
  
Un fournisseur qui encapsule le fournisseur de banque PST doit vérifier régulièrement *ltidNextAlloc* pour voir si elle est NULL. Si tel est le cas, le fournisseur doit remplissez-la avec un nouveau GUID et réinitialiser *dwNextAlloc* afin que les identificateurs d’entrée plus peut être alloué. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

