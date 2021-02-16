---
title: Identificateurs et types de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437216"
---
# <a name="property-identifiers-and-types"></a>Identificateurs et types de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI sont représentées par des balises de propriété. Une balise de propriété est un nombre d’éléments non signés 32 bits qui contient l’identificateur de la propriété dans l’ordre élevé de 16 bits et le type de la propriété dans l’ordre faible de 16 bits. Les balises de propriété pour toutes les propriétés définies par MAPI sont incluses dans le fichier d’en-tête mapitags.h.
  
Les identificateurs de propriété sont utilisés pour indiquer à quoi sert une propriété et qui en est responsable. Les identificateurs de propriété sont divisés par MAPI en plages ; où un identificateur se trouve dans la plage indique son utilisation et sa propriété. 
  
Les types de propriétés sont utilisés pour indiquer le format des données de la propriété. MAPI définit tous les types valides. Les clients et fournisseurs de services qui créent de nouvelles propriétés doivent utiliser l’un de ces types. Tous les types de propriétés sont inclus dans le fichier d’en-tête mapidefs.h.
  

