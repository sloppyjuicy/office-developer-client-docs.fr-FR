---
title: Utilisation d’un tableau pour travailler avec des propriétés
manager: lindalu
ms.date: 02/06/2022
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: Découvrez comment utiliser un tableau pour utiliser des propriétés
ms.openlocfilehash: 85177677ba210e6d910f123dde4bda88a4016d96
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782541"
---
# <a name="using-a-table-to-work-with-properties"></a>Utilisation d’un tableau pour travailler avec des propriétés 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreuses propriétés sont disponibles à la fois à partir des objets qui les prisent en charge et en tant que colonnes sur les tableaux. Dans la mesure du possible, récupérez ces propriétés par le biais du tableau.
  
Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés dont votre client a besoin et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes du tableau. 
  
Ces deux appels sont généralement suffisants pour récupérer suffisamment d’informations à afficher à un utilisateur et sont souvent suffisants pour tout traitement interne nécessaire, en appelant **OpenEntry** pour ouvrir l’objet inutilement. 
  
Il n’existe que deux exceptions :
  
- Si la propriété est de plus de 255 octets. Il **se peut que l’interface IMAPITable** ne retourne pas la valeur entière de la propriété, mais la tronquée à 255 octets. Pensez toutefois à ce compromis. Si vous affichez ces données à l’utilisateur, 255 octets peuvent suffire pour un champ de texte tel qu’un commentaire. 
    
- Si vous avez besoin d’une propriété spécifique d’une seule ligne dans un tableau. Dans ce cas, il est inutile de créer une table avec des propriétés qui ne seront jamais utilisées. La plupart du temps, vous aurez besoin des mêmes propriétés pour toutes les lignes.
