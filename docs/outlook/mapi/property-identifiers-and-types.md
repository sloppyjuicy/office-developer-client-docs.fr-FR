---
title: Types et les identificateurs de propriété
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786937"
---
# <a name="property-identifiers-and-types"></a>Types et les identificateurs de propriété

  
  
**S’applique à**: Outlook 
  
Toutes les propriétés MAPI sont représentées par des balises de propriété. Une balise de propriété est une valeur de nombre entier non signé 32 bits qui contient l’identificateur de la propriété dans le haut niveau de commande 16 bits et le type de propriété dans le bas de commande 16 bits. Balises de propriété pour toutes les propriétés définies par MAPI sont inclus dans le fichier d’en-tête mapitags.h.
  
Identificateurs de propriété sont utilisés pour indiquer qu’une propriété est utilisée pour et qui est responsable. Identificateurs de propriété sont divisées par MAPI plages ; où un identificateur fait partie de la plage indique son utilisation et propriété. 
  
Types de propriété sont utilisés pour indiquer le format des données de la propriété. MAPI définit tous les types valides. Clients et fournisseurs de services de créer de nouvelles propriétés doivent utiliser une de ces types. Tous les types de propriété sont inclus dans le fichier d’en-tête mapidefs.h.
  

