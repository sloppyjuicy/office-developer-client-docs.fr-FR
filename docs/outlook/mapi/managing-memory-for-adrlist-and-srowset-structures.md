---
title: Gestion de la mémoire des structures ADRLIST et SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad3a05a2556512ad06ab52abda29d4bb66fbd605
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561277"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gestion de la mémoire pour les structures ADRLIST et SRowSet »

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’exigence d’allouer toute la mémoire pour une mémoire tampon chaque fois que possible avec un seul appel **MAPIAllocateBuffer** ne s’applique pas lors de l’utilisation de la liste d’adresses, ou **ADRLIST**, et ensemble de lignes, ou **SRowSet**, structures. 
  
Ces deux structures sont des exceptions aux règles standard d’allocation et de libération de mémoire. Ils contiennent plusieurs niveaux de structures et sont conçus pour permettre à des membres individuels d’être ajoutés ou supprimés. Par conséquent, chaque propriété doit être une allocation distincte. 

Lorsque la plupart des structures sont libérées avec un appel à **MAPIFreeBuffer**, chaque entrée individuelle dans une structure **ADRLIST** ou **SRowSet** doit être libérée avec son propre appel à **MAPIFreeBuffer** ou un seul appel à **FreeProws** ou **FreePadrlist**. Pour plus d’informations, [voir MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)et [SRowSet](srowset.md). 

**FreeProws et** **FreePadrlist** sont des fonctions fournies par MAPI pour simplifier la libération de ces structures de données. Pour plus d’informations, [voir FreeProws](freeprows.md) et [FreePadrlist.](freepadrlist.md) **FreePadrlist** libère la mémoire de la structure **ADRLIST** ainsi que toute la mémoire associée pour les membres de la structure . **FreeProws fait** de même pour la structure **SRowSet.** 
  
Le diagramme suivant illustre la disposition d’une structure de données **ADRLIST,** indiquant les allocations de mémoire distinctes requises. Les zones grises indiquent la mémoire qui peut être allouée et libérée avec un seul appel. 
  
**Allocation de mémoire ADRLIST**
  
![Allocation de mémoire ADRLIST](media/amapi_52.gif "Allocation de mémoire ADRLIST")
  
## <a name="see-also"></a>Voir aussi

- [Gestion de la mémoire dans MAPI](managing-memory-in-mapi.md)

