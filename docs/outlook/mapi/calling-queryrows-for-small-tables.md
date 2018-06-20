---
title: Appel QueryRows pour les petites Tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782990"
---
# <a name="calling-queryrows-for-small-tables"></a>Appel QueryRows pour les petites Tables

  
  
**S’applique à**: Outlook 
  
Lors de l’extraction des lignes d’une table de petite taille, appel [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de la première création d’une restriction. Création d’une restriction affecte les performances, car le fournisseur doit d’abord créer un tableau, recherchez les lignes correspondantes dans la table d’origine et puis copiez les lignes à la nouvelle table. Si le nombre total de lignes dans le tableau est inférieure à 100, il est probablement plus efficace lire toutes les lignes et ensuite appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne adéquate. Il s’agit d’une stratégie particulièrement si ces informations sont nécessaires seulement occasionnellement. 
  
Moment propice pour utiliser une restriction est lorsque les informations restreintes ou filtrées seront utilisées sur une période plus longue ou fréquemment utilisées. Par exemple, si vous avez toujours besoin d’un affichage avec des messages non lus, une restriction est l’appel appropriée à utiliser.
  

