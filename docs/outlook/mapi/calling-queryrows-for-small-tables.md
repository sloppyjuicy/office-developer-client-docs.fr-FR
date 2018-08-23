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
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589335"
---
# <a name="calling-queryrows-for-small-tables"></a>Appel de QueryRows pour les petites tables

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lors de l’extraction des lignes d’une table de petite taille, appel [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de la première création d’une restriction. Création d’une restriction affecte les performances, car le fournisseur doit d’abord créer un tableau, recherchez les lignes correspondantes dans la table d’origine et puis copiez les lignes à la nouvelle table. Si le nombre total de lignes dans le tableau est inférieure à 100, il est probablement plus efficace lire toutes les lignes et ensuite appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne adéquate. Il s’agit d’une stratégie particulièrement si ces informations sont nécessaires seulement occasionnellement. 
  
Moment propice pour utiliser une restriction est lorsque les informations restreintes ou filtrées seront utilisées sur une période plus longue ou fréquemment utilisées. Par exemple, si vous avez toujours besoin d’un affichage avec des messages non lus, une restriction est l’appel appropriée à utiliser.
  

