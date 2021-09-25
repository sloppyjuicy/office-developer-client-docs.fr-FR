---
title: Appel de QueryRows pour les petites tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0628d2fcd014b902855cefafb3c2a0603e9157fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605131"
---
# <a name="calling-queryrows-for-small-tables"></a>Appel de QueryRows pour les petites tables

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous récupérez des lignes à partir d’une petite table, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de créer d’abord une restriction. La création d’une restriction a une incidence sur les performances, car le fournisseur doit d’abord créer une table, rechercher les lignes correspondantes dans la table d’origine, puis copier les lignes dans la nouvelle table. Si le nombre total de lignes du tableau est inférieur à 100, il est probablement plus efficace de lire toutes les lignes, puis d’appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne appropriée. Il s’agit d’une stratégie particulièrement efficace si ces informations ne sont nécessaires qu’occasionnellement. 
  
Le moment approprié pour utiliser une restriction est le moment où les informations restreintes ou filtrées sont utilisées sur une période plus longue ou fréquemment. Par exemple, si vous avez toujours besoin d’une vue avec des messages non lus, une restriction est l’appel approprié à utiliser.
  

