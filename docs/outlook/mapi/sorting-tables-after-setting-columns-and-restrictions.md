---
title: Tri des tableaux après la définition de colonnes et de restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409880"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tableaux après la définition de colonnes et de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous devez limiter l’affichage d’une table triée, faites toujours les appels **IMAPITable** suivants dans l’ordre suivant : 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir le jeu de colonnes. 
    
2. [IMAPITable::Restrict](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si la table triée est classée, appelez [IMAPITable::SetCollapseState,](imapitable-setcollapsestate.md)si nécessaire, après l’appel **sortTable.** Cet ordre des appels est important, car la plupart des fournisseurs de services trient un tableau en tant que dernière tâche pour obtenir les meilleures performances. Si, par exemple, un fournisseur de magasins de messages doit catégoriser une table de contenu de dossiers avant qu’une restriction puisse être imposée, cette catégorisation sera supprimée pendant le traitement de la restriction. Une deuxième catégorisation sera nécessaire. 
  

