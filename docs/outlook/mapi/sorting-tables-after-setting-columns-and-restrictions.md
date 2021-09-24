---
title: Tri des tableaux après la définition de colonnes et de restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad28db9be13b18b71b57e0cdae82529f3d4483ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549895"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tableaux après la définition de colonnes et de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous devez limiter l’affichage d’une table triée, faites toujours les appels **IMAPITable** suivants dans l’ordre suivant : 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir le jeu de colonnes. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si la table triée est classée, appelez [IMAPITable::SetCollapseState,](imapitable-setcollapsestate.md)si nécessaire, après l’appel **sortTable.** Cet ordre des appels est important, car la plupart des fournisseurs de services trient un tableau en tant que dernière tâche pour obtenir les meilleures performances. Si, par exemple, un fournisseur de magasins de messages doit catégoriser une table de contenu de dossiers avant qu’une restriction puisse être imposée, cette catégorisation sera supprimée pendant le traitement de la restriction. Une deuxième catégorisation sera nécessaire. 
  

