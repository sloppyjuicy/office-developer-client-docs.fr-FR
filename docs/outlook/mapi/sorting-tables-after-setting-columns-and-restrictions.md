---
title: Tri des tableaux après avoir défini les Restrictions et les colonnes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787234"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Tri des tableaux après avoir défini les Restrictions et les colonnes

  
  
**S’applique à**: Outlook 
  
Lorsque vous avez besoin limiter l’affichage d’une table triée, constituent les appels **IMAPITable** suivants dans l’ordre suivant : 
  
1. [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir l’ensemble de la colonne. 
    
2. [IMAPITable](imapitable-restrict.md) pour imposer la restriction. 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri. 
    
Si le tableau trié est classé, passer un appel à [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l’appel de **SortTable** . Ce classement d’appels est important parce que la plupart des fournisseurs de services de trier un tableau en tant que la dernière tâche pour optimiser les performances. Si, par exemple, un fournisseur de magasin de message doit classer un tableau contenu de dossier avant une restriction peut être imposée, cette catégorisation est supprimée lors du traitement de la restriction. Une deuxième catégorisation est nécessaire. 
  

