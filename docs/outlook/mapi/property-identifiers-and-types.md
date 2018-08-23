---
title: Types et identificateurs de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 423992e0485e8e3092cfc4126164576906d51149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567062"
---
# <a name="property-identifiers-and-types"></a>Types et identificateurs de propriétés

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI sont représentées par des balises de propriété. Une balise de propriété est une valeur de nombre entier non signé 32 bits qui contient l’identificateur de la propriété dans le haut niveau de commande 16 bits et le type de propriété dans le bas de commande 16 bits. Balises de propriété pour toutes les propriétés définies par MAPI sont inclus dans le fichier d’en-tête mapitags.h.
  
Identificateurs de propriété sont utilisés pour indiquer qu’une propriété est utilisée pour et qui est responsable. Identificateurs de propriété sont divisées par MAPI plages ; où un identificateur fait partie de la plage indique son utilisation et propriété. 
  
Types de propriété sont utilisés pour indiquer le format des données de la propriété. MAPI définit tous les types valides. Clients et fournisseurs de services de créer de nouvelles propriétés doivent utiliser une de ces types. Tous les types de propriété sont inclus dans le fichier d’en-tête mapidefs.h.
  

