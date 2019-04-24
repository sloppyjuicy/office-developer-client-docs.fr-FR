---
title: Balises de propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328233"
---
# <a name="mapi-property-tags"></a><span data-ttu-id="a29c2-103">Balises de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="a29c2-103">MAPI property tags</span></span>
  
<span data-ttu-id="a29c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a29c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a29c2-105">Une balise de propriété est un nombre de 32 bits qui contient un identificateur de propriété unique en bits 16 à 31 et un type de propriété en bits 0 à 15, comme indiqué dans l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="a29c2-105">A property tag is a 32-bit number that contains a unique property identifier in bits 16 through 31 and a property type in bits 0 through 15 as shown in the following illustration.</span></span> 
  
<span data-ttu-id="a29c2-106">**Éléments de balise de propriété**</span><span class="sxs-lookup"><span data-stu-id="a29c2-106">**Property tag elements**</span></span>
  
<span data-ttu-id="a29c2-107">![Éléments] de baliSe de propriété (media/amapi_10.gif "Éléments") de baliSe de propriété</span><span class="sxs-lookup"><span data-stu-id="a29c2-107">![Property tag elements](media/amapi_10.gif "Property tag elements")</span></span>
  
<span data-ttu-id="a29c2-108">Les balises de propriété sont utilisées pour identifier les propriétés MAPI et chaque propriété doit en avoir un, que la propriété soit définie par MAPI, un client ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="a29c2-108">Property tags are used to identify MAPI properties and every property must have one, regardless of whether the property is defined by MAPI, a client, or a service provider.</span></span> <span data-ttu-id="a29c2-109">MAPI définit un ensemble de constantes de balise de propriété pour ses propriétés dans le fichier d'en-tête Mapitags. h; ces propriétés sont désignées par le titre «propriétés définies par MAPI».</span><span class="sxs-lookup"><span data-stu-id="a29c2-109">MAPI defines a set of property tag constants for its properties in the Mapitags.h header file; these properties are referred to as the "MAPI-defined properties".</span></span> 
  
<span data-ttu-id="a29c2-110">Les constantes de balise property suivent une convention d'affectation de noms pour la cohérence et la facilité d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="a29c2-110">The property tag constants follow a naming convention for consistency and ease of use.</span></span> <span data-ttu-id="a29c2-111">Le nom de chaque balise de propriété se répartit en deux parties: un préfixe PR_ et une ou plusieurs chaînes de caractères qui décrivent le contenu de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a29c2-111">There are two parts to the name of each property tag: a PR_ prefix and one or more character strings that describe the contents of the property.</span></span> <span data-ttu-id="a29c2-112">Les chaînes de caractères multiples sont séparées par des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="a29c2-112">Multiple character strings are separated by underscores.</span></span> <span data-ttu-id="a29c2-113">Par exemple, la balise de propriété pour le type d'adresse d'un destinataire de message est **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) et l'identificateur d'entrée du dossier désigné pour recevoir une copie de chaque message sortant est **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a29c2-113">For example, the property tag for the address type of a message recipient is **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) and the entry identifier for the folder designated to receive a copy of every outbound message is **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
  
<span data-ttu-id="a29c2-114">Quelques macros sont disponibles pour vous aider à utiliser les balises de propriété, parmi celles-ci [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)et [PROP_TAG](prop_tag.md).</span><span class="sxs-lookup"><span data-stu-id="a29c2-114">A few macros are available to help work with property tags, among them [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md), and [PROP_TAG](prop_tag.md).</span></span> <span data-ttu-id="a29c2-115">**Type\_prop** extrait le type de propriété de la balise de propriété; **ID\_de prop** extrait l'identificateur.</span><span class="sxs-lookup"><span data-stu-id="a29c2-115">**PROP\_TYPE** extracts the property type from the property tag; **PROP\_ID** extracts the identifier.</span></span> <span data-ttu-id="a29c2-116">**PROP_TAG** crée une balise de propriété à partir d'un type et d'un identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="a29c2-116">**PROP_TAG** builds a property tag from a property type and identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a29c2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a29c2-117">See also</span></span>

- [<span data-ttu-id="a29c2-118">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="a29c2-118">MAPI Property Overview</span></span>](mapi-property-overview.md)

