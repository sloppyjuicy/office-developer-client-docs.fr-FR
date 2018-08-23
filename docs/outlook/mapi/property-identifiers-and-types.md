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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="fcca4-103">Types et identificateurs de propriétés</span><span class="sxs-lookup"><span data-stu-id="fcca4-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="fcca4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcca4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcca4-105">Toutes les propriétés MAPI sont représentées par des balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="fcca4-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="fcca4-106">Une balise de propriété est une valeur de nombre entier non signé 32 bits qui contient l’identificateur de la propriété dans le haut niveau de commande 16 bits et le type de propriété dans le bas de commande 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fcca4-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="fcca4-107">Balises de propriété pour toutes les propriétés définies par MAPI sont inclus dans le fichier d’en-tête mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="fcca4-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="fcca4-108">Identificateurs de propriété sont utilisés pour indiquer qu’une propriété est utilisée pour et qui est responsable.</span><span class="sxs-lookup"><span data-stu-id="fcca4-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="fcca4-109">Identificateurs de propriété sont divisées par MAPI plages ; où un identificateur fait partie de la plage indique son utilisation et propriété.</span><span class="sxs-lookup"><span data-stu-id="fcca4-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="fcca4-110">Types de propriété sont utilisés pour indiquer le format des données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="fcca4-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="fcca4-111">MAPI définit tous les types valides.</span><span class="sxs-lookup"><span data-stu-id="fcca4-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="fcca4-112">Clients et fournisseurs de services de créer de nouvelles propriétés doivent utiliser une de ces types.</span><span class="sxs-lookup"><span data-stu-id="fcca4-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="fcca4-113">Tous les types de propriété sont inclus dans le fichier d’en-tête mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="fcca4-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

