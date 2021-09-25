---
title: Utilisation d’un tableau pour travailler avec des propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: abef70e2d5e9fc2eef1ae07f33552c84ecbe9e23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609207"
---
# <a name="using-a-table-to-work-with-properties"></a>Utilisation d’un tableau pour travailler avec des propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreuses propriétés sont disponibles à la fois à partir des objets qui les prisent en charge et en tant que colonnes sur les tableaux. Dans la mesure du possible, récupérez ces propriétés par le biais du tableau.
  
Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés dont votre client a besoin et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes du tableau. 
  
Ces deux appels sont généralement suffisants pour récupérer suffisamment d’informations à afficher à un utilisateur et sont souvent suffisants pour tout traitement interne nécessaire, en appelant **OpenEntry** pour ouvrir l’objet inutilement. 
  
Il n’existe que deux exceptions :
  
- Si la propriété est de plus de 255 octets. L’interface ** IMAPITable ** peut ne pas renvoyer la valeur de la propriété entière, mais la tronquée à 255 octets. Pensez toutefois à ce compromis. Si vous affichez ces données à l’utilisateur, 255 octets peuvent suffire pour un champ de texte tel qu’un commentaire. 
    
- Si vous avez besoin d’une propriété spécifique d’une seule ligne dans un tableau. Dans ce cas, il est inutile de créer une table avec des propriétés qui ne seront jamais utilisées. La plupart du temps, vous aurez besoin des mêmes propriétés pour toutes les lignes.
    

