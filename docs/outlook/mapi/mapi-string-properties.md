---
title: Propriétés de type chaîne MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3cf118866bbc305678201a42a9a91998334f5cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784713"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="f0069-103">Propriétés de type chaîne MAPI</span><span class="sxs-lookup"><span data-stu-id="f0069-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="f0069-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0069-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0069-105">MAPI propose trois différents types de propriété pour décrire les propriétés de type chaîne :</span><span class="sxs-lookup"><span data-stu-id="f0069-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="f0069-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="f0069-106">PT_TSTRING</span></span>
  
<span data-ttu-id="f0069-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f0069-107">PT_STRING8</span></span>
  
<span data-ttu-id="f0069-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0069-108">PT_UNICODE</span></span>
  
<span data-ttu-id="f0069-109">Propriétés de type chaîne sont généralement définies comme PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="f0069-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="f0069-110">Le type de propriété PT_TSTRING compilation conditionnelle à un des autres types de propriété de chaîne, selon selon si la macro UNICODE a été définie.</span><span class="sxs-lookup"><span data-stu-id="f0069-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="f0069-111">PT_STRING8 décrit des chaînes de caractères terminée par le caractère null de 8 bits au format ANSI ; PT_UNICODE décrit les chaînes de caractères terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="f0069-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="f0069-112">Soit un client ou un fournisseur de services, ou à la fois client et fournisseur la possibilité de prendre en charge des chaînes de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0069-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="f0069-113">Il n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0069-113">It is not required.</span></span> <span data-ttu-id="f0069-114">Un client qui prend en charge uniquement les chaînes PT_STRING8 peut fonctionner avec un fournisseur qui prend en charge Unicode et vice versa.</span><span class="sxs-lookup"><span data-stu-id="f0069-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="f0069-115">Pour activer cette interopérabilité, clients et fournisseurs de services de transmettent un indicateur, l’indicateur MAPI_UNICODE, pour indiquer que Unicode est pris en charge dans les méthodes qui impliquent l’échange des chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="f0069-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="f0069-116">Par exemple, supposons qu’un client prend en charge Unicode et a besoin de récupérer le nom complet d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="f0069-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="f0069-117">Toutes les propriétés PT_TSTRING du client sont compilés en type PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f0069-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="f0069-118">Lorsque le client appelle la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) du dossier à récupérer sa propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), il passe l’indicateur MAPI_UNICODE pour demander que renvoyer la chaîne du nom complet dans le format Unicode .</span><span class="sxs-lookup"><span data-stu-id="f0069-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="f0069-119">Fournisseurs de services et les clients doivent connaître spécifiant un jeu de caractères dans un appel de méthode est uniquement une demande.</span><span class="sxs-lookup"><span data-stu-id="f0069-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="f0069-120">Prise en charge d’un ou deux jeux de caractères dépend de l’implémentation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f0069-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="f0069-121">Toutefois, les fournisseurs de services sont invités à prendre en charge les deux jeux de caractères, car il leur permet d’atteindre la distribution plus large que les fournisseurs qui prennent en charge qu’un seul ensemble.</span><span class="sxs-lookup"><span data-stu-id="f0069-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="f0069-122">Propriétés de type chaîne peuvent devenir très volumineux comme propriétés binaires, les propriétés qui utilisent la propriété type PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="f0069-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="f0069-123">Pour faciliter l’utilisation des propriétés de grande taille, MAPI permet de fournisseurs de services de définition de ces propriétés appliquer des limites de taille.</span><span class="sxs-lookup"><span data-stu-id="f0069-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="f0069-124">Ces limites peuvent varier, en fonction de :</span><span class="sxs-lookup"><span data-stu-id="f0069-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="f0069-125">Indique si les propriétés sont en cours lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="f0069-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="f0069-126">Comment le fournisseur de services implémente les méthodes **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="f0069-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="f0069-127">Considérations de runtime, telles que des contraintes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f0069-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="f0069-128">Problèmes de traduction du jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="f0069-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="f0069-129">Limites de taille peuvent également être placés sur une chaîne et propriétés binaires lorsqu’ils sont utilisés dans la colonne valeur d’une table car il est parfois impossible afficher tous les valeur d’une propriété de grande taille.</span><span class="sxs-lookup"><span data-stu-id="f0069-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="f0069-130">Plusieurs fournisseurs de services tronquent la chaîne de grande taille ou des propriétés binaires qui sont utilisées dans les tableaux à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="f0069-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="f0069-131">Lorsqu’un client appelle la méthode **GetProps** ou **SetProps** d’un objet pour travailler avec une chaîne de grande taille ou une propriété binaire et l’appel échoue en raison de la taille de la propriété, la méthode renvoie la valeur d’erreur MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="f0069-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="f0069-132">S’il est **GetProps** qui ont échoué pour une propriété spécifique, le client peut récupérer en appelant [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et en demandant **IStream** pour l’accès en spécifiant l’identificateur d’interface IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="f0069-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="f0069-133">À l’aide de **OpenProperty**, le client peut extraire une propriété de grande taille à l’aide d’une interface comme **IStream** qui convient mieux pour l’utilisation des propriétés de grande taille.</span><span class="sxs-lookup"><span data-stu-id="f0069-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0069-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0069-134">See also</span></span>



[<span data-ttu-id="f0069-135">Vue d'ensemble de la propri�t� MAPI</span><span class="sxs-lookup"><span data-stu-id="f0069-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

