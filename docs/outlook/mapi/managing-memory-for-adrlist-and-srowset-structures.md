---
title: Gestion de la mémoire des structures ADRLIST et SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298126"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gestion de la mémoire pour les structures ADRLIST et SRowSet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La nécessité d'allouer toute la mémoire d'une mémoire tampon dans la mesure du possible avec un seul appel **MAPIAllocateBuffer** ne s'applique pas lorsque vous utilisez la liste d'adresses, ou **ADRLIST**et le jeu de lignes, ou **SRowSet**, structures. 
  
Ces deux structures sont des exceptions aux règles standard d'allocation et de libération de mémoire. Elles contiennent plusieurs niveaux de structures et sont conçues pour permettre l'ajout ou la suppression de membres individuels. Par conséquent, chaque propriété doit être une allocation distincte. 

Lorsque la plupart des structures sont libérées à l'aide d'un appel à **MAPIFreeBuffer**, chaque entrée individuelle d'une structure **ADRLIST** ou **SRowSet** doit être libérée avec son propre appel à **MAPIFreeBuffer** ou un seul appel à **FreeProws** ou ** FreePadrlist**. Pour plus d'informations, voir [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)et [SRowSet](srowset.md). 

**FreeProws** et **FreePadrlist** sont des fonctions fournies par MAPI pour simplifier la libération de ces structures de données. Pour plus d'informations, voir [FreeProws](freeprows.md) et [FreePadrlist](freepadrlist.md). **FreePadrlist** libère la mémoire de la structure **ADRLIST** plus l'ensemble de la mémoire associée aux membres de la structure; **FreeProws** effectue la même opération pour la structure **SRowSet** . 
  
Le diagramme suivant montre la disposition d'une structure de données **ADRLIST** , indiquant les allocations de mémoire distinctes requises. Les cases gris affichent de la mémoire qui peut être allouée et libérée en un seul appel. 
  
**Allocation de mémoire ADRLIST**
  
![Allocation de mémoire ADRLIST] (media/amapi_52.gif "Allocation de mémoire ADRLIST")
  
## <a name="see-also"></a>Voir aussi

- [Gestion de la mémoire dans MAPI](managing-memory-in-mapi.md)

