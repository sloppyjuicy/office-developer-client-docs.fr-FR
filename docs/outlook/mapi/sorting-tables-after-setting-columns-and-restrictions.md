---
title: Tri des tables après la définition des colonnes et des restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f975ed1b9036bce5ed225b2a9020262260f4f57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572143"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tables après la définition des colonnes et des restrictions

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous avez besoin limiter l’affichage d’une table triée, constituent les appels **IMAPITable** suivants dans l’ordre suivant : 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir l’ensemble de la colonne. 
    
2. [IMAPITable](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si le tableau trié est classé, passer un appel à [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l’appel de **SortTable** . Ce classement d’appels est important parce que la plupart des fournisseurs de services de trier un tableau en tant que la dernière tâche pour optimiser les performances. Si, par exemple, un fournisseur de magasin de message doit classer un tableau contenu de dossier avant une restriction peut être imposée, cette catégorisation est supprimée lors du traitement de la restriction. Une deuxième catégorisation est nécessaire. 
  

