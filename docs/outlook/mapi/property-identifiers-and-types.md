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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="0f631-103">Identificateurs et types de propriétés</span><span class="sxs-lookup"><span data-stu-id="0f631-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="0f631-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f631-105">Toutes les propriétés MAPI sont représentées par des balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="0f631-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="0f631-106">Une balise de propriété est un nombre d’éléments non signés 32 bits qui contient l’identificateur de la propriété dans l’ordre élevé de 16 bits et le type de la propriété dans l’ordre faible de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0f631-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="0f631-107">Les balises de propriété pour toutes les propriétés définies par MAPI sont incluses dans le fichier d’en-tête mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="0f631-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="0f631-108">Les identificateurs de propriété sont utilisés pour indiquer à quoi sert une propriété et qui en est responsable.</span><span class="sxs-lookup"><span data-stu-id="0f631-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="0f631-109">Les identificateurs de propriété sont divisés par MAPI en plages ; où un identificateur se trouve dans la plage indique son utilisation et sa propriété.</span><span class="sxs-lookup"><span data-stu-id="0f631-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="0f631-110">Les types de propriétés sont utilisés pour indiquer le format des données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0f631-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="0f631-111">MAPI définit tous les types valides.</span><span class="sxs-lookup"><span data-stu-id="0f631-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="0f631-112">Les clients et fournisseurs de services qui créent de nouvelles propriétés doivent utiliser l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="0f631-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="0f631-113">Tous les types de propriétés sont inclus dans le fichier d’en-tête mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="0f631-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

