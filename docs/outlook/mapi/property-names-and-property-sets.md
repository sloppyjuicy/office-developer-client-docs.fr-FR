---
title: Les noms de propriétés et les jeux de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786977"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="020a4-103">Les noms de propriétés et les jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="020a4-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="020a4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="020a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="020a4-105">Le nom de chaque propriété nommée comporte deux parties :</span><span class="sxs-lookup"><span data-stu-id="020a4-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="020a4-106">Un identificateur global unique, ou le GUID, qui spécifie un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="020a4-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="020a4-107">Une chaîne de caractères Unicode ou une valeur numérique 32 bits.</span><span class="sxs-lookup"><span data-stu-id="020a4-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="020a4-108">Noms des propriétés nommées sont décrites à l’aide d’une structure [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="020a4-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="020a4-109">Cette structure contient un membre de jeu de propriétés, un membre pour indiquer le nom de format numérique ou chaîne et un membre pour identifier le format est utilisé.</span><span class="sxs-lookup"><span data-stu-id="020a4-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="020a4-110">Étant donné que le jeu de propriétés fait partie du nom de la propriété, il n’est pas facultatif.</span><span class="sxs-lookup"><span data-stu-id="020a4-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="020a4-111">MAPI a défini plusieurs jeux de propriétés pour une utilisation par les clients et les fournisseurs de service, mais si un ensemble existant de la propriété est inapproprié, un nouveau jeu de propriétés peut être défini.</span><span class="sxs-lookup"><span data-stu-id="020a4-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="020a4-112">Clients et fournisseurs de services peuvent définir leurs propres jeux de propriétés en appelant la fonction [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="020a4-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) function.</span></span> <span data-ttu-id="020a4-113">Ces jeux de propriétés est généralement créés pour les applications clientes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="020a4-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="020a4-114">Jeux de propriétés de MAPI sont représentés par l’une des constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="020a4-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="020a4-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="020a4-115">PS_MAPI</span></span>
  
<span data-ttu-id="020a4-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="020a4-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="020a4-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="020a4-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="020a4-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="020a4-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="020a4-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="020a4-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="020a4-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="020a4-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="020a4-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="020a4-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="020a4-122">Le jeu de propriétés PS_MAPI est réservé. Il est utilisé par les fournisseurs de services pour générer des noms des propriétés avec des identificateurs au-dessous de la plage de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="020a4-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="020a4-123">Le jeu de propriétés PS_PUBLIC_STRINGS est utilisé par les clients pour les propriétés nommées de messages IPM.</span><span class="sxs-lookup"><span data-stu-id="020a4-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="020a4-124">Étant donné que les propriétés nommées dans le jeu de propriétés PS_PUBLIC_STRINGS apparaissent dans l’interface utilisateur d’un client, messages non telles que celles qui appartiennent à la classe de message IPC Évitez de créer des propriétés avec ce jeu de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="020a4-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="020a4-125">Au lieu de cela, ils doivent créer des propriétés de la plage de spécifiques à la classe de message, 0x6800 via 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="020a4-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="020a4-126">Les autres jeux de propriétés contiennent des propriétés nommées décrivant les destinataires qui sont généralement des membres d’une liste de routage.</span><span class="sxs-lookup"><span data-stu-id="020a4-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="020a4-127">Contenant le même type d’informations que les propriétés qui sont associées aux propriétés de la liste de destinataires, les propriétés de ces jeux de propriétés sont entendent par des passerelles nécessiter un mappage pour un système de messagerie cible.</span><span class="sxs-lookup"><span data-stu-id="020a4-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="020a4-128">Car il existe cinq types d’informations pour décrire les propriétés, MAPI a défini cinq jeux de propriétés différentes.</span><span class="sxs-lookup"><span data-stu-id="020a4-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="020a4-129">Un client envoie un message qui doit inclure une adresse et le type d’adresse pour ses membres de la liste Routage affecte une propriété nommée pour chaque membre de la PS_ROUTING_EMAIL_ADDRESSES et la propriété PS_ROUTING_ADDRTYPE définit.</span><span class="sxs-lookup"><span data-stu-id="020a4-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="020a4-130">Cela garantit que l’adresse et le type d’adresse viabilité lorsque envoyé à un système de messagerie étranger.</span><span class="sxs-lookup"><span data-stu-id="020a4-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="020a4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="020a4-131">See also</span></span>



[<span data-ttu-id="020a4-132">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="020a4-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

