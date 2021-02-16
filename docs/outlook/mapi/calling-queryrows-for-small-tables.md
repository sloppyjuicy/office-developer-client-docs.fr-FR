---
title: Appel de QueryRows pour les petites tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404175"
---
# <a name="calling-queryrows-for-small-tables"></a>Appel de QueryRows pour les petites tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous récupérez des lignes à partir d’une petite table, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de créer d’abord une restriction. La création d’une restriction a un impact sur les performances, car le fournisseur doit d’abord créer une table, rechercher les lignes correspondantes dans la table d’origine, puis copier les lignes dans la nouvelle table. Si le nombre total de lignes du tableau est inférieur à 100, il est probablement plus efficace de lire toutes les lignes, puis d’appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne appropriée. Il s’agit d’une stratégie particulièrement efficace si ces informations ne sont nécessaires qu’occasionnellement. 
  
Le moment approprié pour utiliser une restriction est le moment où les informations restreintes ou filtrées sont utilisées sur une période plus longue ou fréquemment. Par exemple, si vous avez toujours besoin d’un affichage avec des messages non lus, une restriction est l’appel approprié à utiliser.
  

