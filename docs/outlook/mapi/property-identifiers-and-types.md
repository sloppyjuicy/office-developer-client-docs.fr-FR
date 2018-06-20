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
# <a name="property-identifiers-and-types"></a><span data-ttu-id="a9649-103">Types et les identificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="a9649-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="a9649-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9649-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9649-105">Toutes les propriétés MAPI sont représentées par des balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="a9649-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="a9649-106">Une balise de propriété est une valeur de nombre entier non signé 32 bits qui contient l’identificateur de la propriété dans le haut niveau de commande 16 bits et le type de propriété dans le bas de commande 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a9649-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="a9649-107">Balises de propriété pour toutes les propriétés définies par MAPI sont inclus dans le fichier d’en-tête mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="a9649-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="a9649-108">Identificateurs de propriété sont utilisés pour indiquer qu’une propriété est utilisée pour et qui est responsable.</span><span class="sxs-lookup"><span data-stu-id="a9649-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="a9649-109">Identificateurs de propriété sont divisées par MAPI plages ; où un identificateur fait partie de la plage indique son utilisation et propriété.</span><span class="sxs-lookup"><span data-stu-id="a9649-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="a9649-110">Types de propriété sont utilisés pour indiquer le format des données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a9649-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="a9649-111">MAPI définit tous les types valides.</span><span class="sxs-lookup"><span data-stu-id="a9649-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="a9649-112">Clients et fournisseurs de services de créer de nouvelles propriétés doivent utiliser une de ces types.</span><span class="sxs-lookup"><span data-stu-id="a9649-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="a9649-113">Tous les types de propriété sont inclus dans le fichier d’en-tête mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="a9649-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

