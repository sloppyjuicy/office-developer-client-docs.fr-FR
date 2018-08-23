---
title: Gestion de la mémoire pour les structures ADRLIST et SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589727"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gestion de la mémoire pour les structures ADRLIST et SRowSet »

**S’applique à**: Outlook 2013 | Outlook 2016 
  
La condition requise pour allouer toute la mémoire pour une mémoire tampon de la mesure du possible avec un seul appel **MAPIAllocateBuffer** ne s’applique pas à l’aide de la liste d’adresses ou **ADRLIST**et jeu de lignes ou **SRowSet**, structures. 
  
Ces deux structures sont des exceptions pour les règles standards d’allouer et de libérer de la mémoire. Ils contiennent plusieurs niveaux de structures et sont conçues pour permettre aux membres individuels être ajouté ou supprimé. Par conséquent, chaque propriété doit être une affectation distincte. 

Où la plupart des structures sont libérées par un appel à **MAPIFreeBuffer**, chaque entrée individuelle dans une structure **ADRLIST** ou **SRowSet** doivent être libérée avec son propre appel à **MAPIFreeBuffer** ou un seul appel **FreeProws** ou ** FreePadrlist**. Pour plus d’informations, voir [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)et [SRowSet](srowset.md). 

**FreeProws** et **FreePadrlist** sont des fonctions fournies par MAPI pour simplifier la libération de ces structures de données. Pour plus d’informations, voir [FreeProws](freeprows.md) et [FreePadrlist](freepadrlist.md). **FreePadrlist** libère de la mémoire pour la structure **ADRLIST** plus de mémoire tous les membres de la structure ; **FreeProws** effectue la même pour la structure **SRowSet** . 
  
Le diagramme suivant illustre la disposition d’une structure de données **ADRLIST** , indiquant les allocations de mémoire distinct requises. Les zones grisées indiquent la mémoire pouvant être allouée et publié avec un seul appel. 
  
**Allocation de mémoire ADRLIST**
  
![Allocation de mémoire ADRLIST] (media/amapi_52.gif "Allocation de mémoire ADRLIST")
  
## <a name="see-also"></a>Voir aussi

- [Gestion de la mémoire dans MAPI](managing-memory-in-mapi.md)

