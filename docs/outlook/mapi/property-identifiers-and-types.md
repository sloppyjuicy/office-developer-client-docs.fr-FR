---
title: Types et identificateurs de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328538"
---
# <a name="property-identifiers-and-types"></a>Types et identificateurs de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI sont représentées par des balises de propriété. Une balise de propriété est une valeur entière non signée de 32 bits qui contient l'identificateur de la propriété dans l'ordre haut 16 bits et le type de la propriété dans la commande basse de 16 bits. Les balises de propriété de toutes les propriétés définies par MAPI sont incluses dans le fichier d'en-tête mapitags. h.
  
Les identificateurs de propriétés sont utilisés pour indiquer ce à quoi une propriété est utilisée et qui est responsable de celle-ci. Les identificateurs de propriétés sont divisés par MAPI en plages; l'emplacement où se trouve un identificateur dans la plage indique son utilisation et sa propriété. 
  
Les types de propriétés sont utilisés pour indiquer le format des données de la propriété. MAPI définit tous les types valides. Les clients et les fournisseurs de services qui créent de nouvelles propriétés doivent utiliser l'un de ces types. Tous les types de propriétés sont inclus dans le fichier d'en-tête mapidefs. h.
  

