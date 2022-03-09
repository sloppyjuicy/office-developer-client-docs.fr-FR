---
title: Tri des tableaux après la définition de colonnes et de restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
ms.openlocfilehash: a4519048808354295eb6ff85b5514a01de157727
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375803"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tableaux après la définition de colonnes et de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous devez limiter l’affichage d’une table triée, faites toujours les appels **IMAPITable** suivants dans l’ordre suivant : 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir le jeu de colonnes. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si la table triée est classée, appelez [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l’appel **sortTable** . Cet ordre des appels est important, car la plupart des fournisseurs de services trient un tableau en tant que dernière tâche pour obtenir les meilleures performances. Si, par exemple, un fournisseur de magasins de messages doit catégoriser une table de contenu de dossiers avant qu’une restriction puisse être imposée, cette catégorisation sera supprimée pendant le traitement de la restriction. Une deuxième catégorisation sera nécessaire. 
  

