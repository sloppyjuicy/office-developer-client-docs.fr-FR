---
title: Utilisation d’une table pour utiliser les propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585422"
---
# <a name="using-a-table-to-work-with-properties"></a>Utilisation d’une table pour utiliser les propriétés

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
De nombreuses propriétés sont disponibles et à partir des objets qui prennent en charge les colonnes de tables. La mesure du possible, extraire ces propriétés par le biais de la table.
  
Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés nécessaires à votre client et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table. 
  
Ces deux appels sont généralement suffisants pour l’extraction de suffisamment d’informations à afficher à l’utilisateur et sont souvent suffisantes pour tout traitement interne nécessaire, un appel à **OpenEntry** pour ouvrir l’objet inutile. 
  
Il existe deux exceptions près :
  
- Si la propriété est supérieure à 255 octets. Le ** IMAPITable ** interface peut ne pas retourne la valeur de propriété entière, au lieu de cela tronque à 255 octets. Pensez à ce compromis, cependant. Si ces données sont affichées à l’utilisateur, 255 octets peut être suffisant pour un champ texte comme un commentaire. 
    
- Si vous avez besoin d’une propriété spécifique à partir d’une seule ligne dans un tableau. Dans ce cas, il est inutile de créer un tableau avec des propriétés qui ne seront jamais utilisées. Plupart du temps, que vous devez les mêmes propriétés pour toutes les lignes.
    

