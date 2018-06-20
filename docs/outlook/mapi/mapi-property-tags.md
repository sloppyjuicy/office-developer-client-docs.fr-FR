---
title: Balises de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8dc37f1b594eeaa199b48f5946d10e60427d4988
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784680"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="9377a-103">Balises de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="9377a-103">MAPI property tags</span></span>
  
<span data-ttu-id="9377a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9377a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9377a-105">Une balise de propriété est un nombre à 32 bits qui contient un identificateur de la propriété unique en bits 31 à 16 et un type de propriété dans les bits 0 à 15, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9377a-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="9377a-106">**Éléments de balise de propriété**</span><span class="sxs-lookup"><span data-stu-id="9377a-106">**Property tag elements**</span></span>
  
<span data-ttu-id="9377a-107">![Éléments de balise de propriété] (media/amapi_10.gif "Éléments de balise de propriété")</span><span class="sxs-lookup"><span data-stu-id="9377a-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="9377a-108">Balises de propriété sont utilisés pour identifier les propriétés MAPI et chaque propriété doit contenir un, indépendamment de si la propriété est définie par MAPI, un client ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="9377a-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="9377a-109">MAPI définit un ensemble de constantes de la propriété tag pour ses propriétés dans le fichier d’en-tête Mapitags.h ; Ces propriétés sont appelées « propriétés définies par le MAPI ».</span><span class="sxs-lookup"><span data-stu-id="9377a-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="9377a-110">Les constantes de balise de propriété suivent une convention d’affectation de noms pour la cohérence et la facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9377a-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="9377a-111">Il existe deux composants sur le nom de chaque balise de propriété : un préfixe PR_ et un ou plusieurs chaînes de caractères qui décrivent le contenu de la propriété.</span><span class="sxs-lookup"><span data-stu-id="9377a-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="9377a-112">Plusieurs chaînes de caractères sont séparés par des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="9377a-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="9377a-113">Par exemple, la balise de propriété pour le type d’adresse d’un destinataire du message est **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) et l’identificateur d’entrée pour le dossier désigné pour recevoir une copie de chaque message sortant est **PR_IPM_SENTMAIL_ Propriété ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9377a-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](http://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="9377a-114">Macros quelques sont disponibles pour aider à travailler avec des balises de propriété entre eux [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)et [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="9377a-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="9377a-115">**PROPRIÉTÉS\_TYPE** extrait le type de propriété de la balise de propriété ; **Propriétés\_ID** extrait l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="9377a-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="9377a-116">**PROP_TAG** génère une balise de propriété à partir d’un identificateur et le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="9377a-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9377a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9377a-117">See also</span></span>

- [<span data-ttu-id="9377a-118">Vue d'ensemble de la propri�t� MAPI</span><span class="sxs-lookup"><span data-stu-id="9377a-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

