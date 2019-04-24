---
title: Tri des tables après la définition des colonnes et des restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344484"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tables après la définition des colonnes et des restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous devez limiter l'affichage d'un tableau trié, effectuez toujours les appels **IMAPITable** suivants dans l'ordre suivant: 
  
1. [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour définir le jeu de colonnes. 
    
2. [IMAPITable:: restreindre](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable:: SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si le tableau trié est classé, effectuez un appel à [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l'appel de **SortTable** . Cette classification des appels est importante, car la plupart des fournisseurs de services trient un tableau en tant que dernière tâche pour obtenir les meilleures performances. Si, par exemple, un fournisseur de banque de messages doit catégoriser une table de contenu de dossier avant qu'une restriction puisse être imposée, cette catégorisation sera supprimée lors du traitement de la restriction. Une deuxième catégorisation sera nécessaire. 
  

