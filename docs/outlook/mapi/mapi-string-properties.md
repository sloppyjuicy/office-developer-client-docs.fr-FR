---
title: Propriétés de chaîne MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431392"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="3f213-103">Propriétés de chaîne MAPI</span><span class="sxs-lookup"><span data-stu-id="3f213-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="3f213-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f213-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f213-105">MAPI fournit trois types de propriétés différents pour décrire les propriétés de chaîne:</span><span class="sxs-lookup"><span data-stu-id="3f213-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="3f213-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="3f213-106">PT_TSTRING</span></span>
  
<span data-ttu-id="3f213-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3f213-107">PT_STRING8</span></span>
  
<span data-ttu-id="3f213-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f213-108">PT_UNICODE</span></span>
  
<span data-ttu-id="3f213-109">Les propriétés de chaîne sont généralement définies comme PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="3f213-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="3f213-110">Le type de propriété PT_TSTRING est compilé de manière conditionnelle sur l'un des autres types de propriété de chaîne, selon que la macro UNICODE a été définie ou non.</span><span class="sxs-lookup"><span data-stu-id="3f213-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="3f213-111">PT_STRING8 décrit les chaînes de caractères de 8 bits se terminant par null au format ANSI; PT_UNICODE décrit les chaînes de caractères codés sur deux octets qui se terminent par null.</span><span class="sxs-lookup"><span data-stu-id="3f213-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="3f213-112">Un fournisseur de services ou client, ou le client et le fournisseur peuvent choisir de prendre en charge les chaînes de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f213-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="3f213-113">Elle n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3f213-113">It is not required.</span></span> <span data-ttu-id="3f213-114">Un client qui prend en charge uniquement les chaînes PT_STRING8 peut fonctionner avec un fournisseur qui prend en charge Unicode, et inversement.</span><span class="sxs-lookup"><span data-stu-id="3f213-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="3f213-115">Pour activer cette interopérabilité, les clients et les fournisseurs de services transmettent un indicateur, l'indicateur MAPI_UNICODE, pour indiquer qu'Unicode est pris en charge dans les méthodes qui impliquent l'échange de chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="3f213-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="3f213-116">Par exemple, supposons qu'un client prend en charge Unicode et qu'il doive récupérer le nom d'affichage d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="3f213-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="3f213-117">Toutes les propriétés PT_TSTRING du client sont compilées en type PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3f213-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="3f213-118">Lorsque le client appelle la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du dossier pour récupérer sa propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), il passe l'indicateur MAPI_UNICODE pour demander que la chaîne de nom d'affichage soit renvoyée au format Unicode. .</span><span class="sxs-lookup"><span data-stu-id="3f213-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="3f213-119">Les clients et fournisseurs de services doivent savoir que la spécification d'un jeu de caractères dans un appel de méthode n'est qu'une requête.</span><span class="sxs-lookup"><span data-stu-id="3f213-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="3f213-120">La prise en charge d'un ou des deux jeux de caractères est jusqu'à l'implémentation de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3f213-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="3f213-121">Toutefois, les fournisseurs de services sont encouragés à prendre en charge les deux jeux de caractères, car cela leur permet d'obtenir une distribution plus répandue que les fournisseurs qui ne prennent en charge qu'un seul ensemble.</span><span class="sxs-lookup"><span data-stu-id="3f213-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="3f213-122">Les propriétés de chaîne peuvent devenir assez volumineuses en ce qui concerne les propriétés binaires, qui utilisent le type de propriété PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="3f213-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="3f213-123">Pour faciliter l'utilisation des propriétés volumineuses, MAPI permet aux fournisseurs de services de définir ces propriétés afin d'appliquer des limites de taille.</span><span class="sxs-lookup"><span data-stu-id="3f213-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="3f213-124">Ces limites peuvent varier en fonction des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="3f213-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="3f213-125">Indique si les propriétés sont en cours de lecture ou d'écriture.</span><span class="sxs-lookup"><span data-stu-id="3f213-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="3f213-126">Comment le fournisseur de services implémente les méthodes **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="3f213-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="3f213-127">Considérations relatives à l'exécution, telles que les contraintes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3f213-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="3f213-128">Problèmes de conversion des jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="3f213-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="3f213-129">Les limites de taille peuvent également être placées sur les propriétés de chaîne et binaires lorsqu'elles sont utilisées dans le jeu de colonnes d'un tableau car il est parfois impossible de rendre entièrement visible la valeur de la propriété large.</span><span class="sxs-lookup"><span data-stu-id="3f213-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="3f213-130">De nombreux fournisseurs de services tronquent les grandes propriétés de chaîne ou binaires qui sont utilisées dans les tableaux à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="3f213-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="3f213-131">Lorsqu'un client appelle la méthode **GetProps** ou **SetProps** d'un objet pour fonctionner avec une chaîne ou une propriété binaire de grande taille et si l'appel échoue en raison de la taille de la propriété, la méthode renvoie la valeur d'erreur MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="3f213-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="3f213-132">S'il s'agit d' **GetProps** qui échoue pour une propriété spécifique, le client peut effectuer une récupération en appelant [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et en demandant à l'accès **IStream** en spécifiant IID_IStream comme identificateur d'interface.</span><span class="sxs-lookup"><span data-stu-id="3f213-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="3f213-133">À l'aide de **OpenProperty**, le client peut récupérer une grande propriété à l'aide d'une interface telle que **IStream** , mieux adaptée à l'utilisation de propriétés volumineuses.</span><span class="sxs-lookup"><span data-stu-id="3f213-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f213-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f213-134">See also</span></span>



[<span data-ttu-id="3f213-135">Vue d’ensemble de la propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="3f213-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

