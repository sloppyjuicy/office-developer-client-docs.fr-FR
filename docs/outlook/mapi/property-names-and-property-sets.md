---
title: Noms des propriétés et jeux de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328545"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="b5569-103">Noms des propriétés et jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="b5569-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="b5569-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5569-105">Le nom de chaque propriété nommée est en deux parties :</span><span class="sxs-lookup"><span data-stu-id="b5569-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="b5569-106">Identificateur global unique, ou GUID, qui spécifie un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5569-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="b5569-107">Chaîne de caractères Unicode ou valeur numérique 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5569-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="b5569-108">Les noms des propriétés nommées sont décrits à l’aide d’une structure [MAPINAMEID.](mapinameid.md)</span><span class="sxs-lookup"><span data-stu-id="b5569-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="b5569-109">Cette structure contient un membre de jeu de propriétés, un membre pour spécifier le nom au format numérique ou de chaîne, et un membre pour identifier le format utilisé.</span><span class="sxs-lookup"><span data-stu-id="b5569-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="b5569-110">Étant donné que le jeu de propriétés fait partie du nom de la propriété, il n’est pas facultatif.</span><span class="sxs-lookup"><span data-stu-id="b5569-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="b5569-111">MAPI a défini plusieurs jeux de propriétés à utiliser par les clients et les fournisseurs de services, mais si un jeu de propriétés existant est inapproprié, un nouveau jeu de propriétés peut être défini.</span><span class="sxs-lookup"><span data-stu-id="b5569-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="b5569-112">Les clients et les fournisseurs de services peuvent définir leurs propres jeux de propriétés en appelant la fonction [CoCreateGUID.](https://msdn.microsoft.com/library/ms688568.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5569-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="b5569-113">En règle générale, ces jeux de propriétés sont créés pour les applications clientes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b5569-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="b5569-114">Les jeux de propriétés MAPI sont représentés par les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5569-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="b5569-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="b5569-115">PS_MAPI</span></span>
  
<span data-ttu-id="b5569-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b5569-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="b5569-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="b5569-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="b5569-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="b5569-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="b5569-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b5569-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="b5569-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="b5569-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="b5569-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b5569-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="b5569-122">Le PS_MAPI de propriétés est réservé ; Il est utilisé par les fournisseurs de services pour générer des noms pour les propriétés dont les identificateurs sont inférieurs à la plage de propriétés nommée.</span><span class="sxs-lookup"><span data-stu-id="b5569-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="b5569-123">Le PS_PUBLIC_STRINGS de propriétés est utilisé par les clients pour les propriétés nommées des messages IPM.</span><span class="sxs-lookup"><span data-stu-id="b5569-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="b5569-124">Étant donné que les propriétés nommées dans le jeu de propriétés PS_PUBLIC_STRINGS apparaissent dans l’interface utilisateur d’un client, les messages nonvisables tels que ceux qui appartiennent à la classe de message IPC doivent éviter de créer des propriétés nommées avec ce jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5569-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="b5569-125">Au lieu de cela, ils doivent créer des propriétés dans la plage spécifique à la classe de message, 0x6800 à 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="b5569-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="b5569-126">Les autres jeux de propriétés ont des propriétés nommées décrivant les destinataires qui sont généralement membres d’une liste de routage.</span><span class="sxs-lookup"><span data-stu-id="b5569-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="b5569-127">Contenant le même type d’informations que les propriétés associées aux propriétés de liste des destinataires, les propriétés de ces jeux de propriétés sont comprises par les passerelles pour exiger un mappage pour un système de messagerie cible.</span><span class="sxs-lookup"><span data-stu-id="b5569-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="b5569-128">Étant donné qu’il existe cinq types d’informations pour décrire les propriétés, MAPI a défini cinq jeux de propriétés différents.</span><span class="sxs-lookup"><span data-stu-id="b5569-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="b5569-129">Un client envoyant un message qui doit inclure une adresse et un type d’adresse pour ses membres de liste de routage affecte une propriété nommée pour chaque membre des jeux de propriétés PS_ROUTING_EMAIL_ADDRESSES et PS_ROUTING_ADDRTYPE de routage.</span><span class="sxs-lookup"><span data-stu-id="b5569-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="b5569-130">Cela garantit que l’adresse et le type d’adresse restent viables lorsqu’ils sont envoyés à un système de messagerie étranger.</span><span class="sxs-lookup"><span data-stu-id="b5569-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5569-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5569-131">See also</span></span>



[<span data-ttu-id="b5569-132">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="b5569-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

