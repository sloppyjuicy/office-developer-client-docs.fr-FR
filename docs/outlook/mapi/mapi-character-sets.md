---
title: Jeux de caractères MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582531"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="fb623-103">Jeux de caractères MAPI</span><span class="sxs-lookup"><span data-stu-id="fb623-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="fb623-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb623-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb623-105">Applications clientes compatibles MAPI et les fournisseurs de services peuvent utiliser des caractères ANSI (octet) ou Unicode (deux octets).</span><span class="sxs-lookup"><span data-stu-id="fb623-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="fb623-106">Jeux de caractères OEM ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fb623-106">OEM character sets are not supported.</span></span> <span data-ttu-id="fb623-107">Une chaîne OEM transmis à une méthode MAPI ou la fonction entraînera cette méthode ou la fonction en échec.</span><span class="sxs-lookup"><span data-stu-id="fb623-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="fb623-108">Les applications clientes qui fonctionnent avec les noms de fichiers dans le jeu de caractères OEM doivent être prudent pour les convertir au format ANSI avant de les passer à une méthode MAPI ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="fb623-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="fb623-109">Prise en charge Unicode jeu de caractères est facultatif, à la fois pour les clients et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="fb623-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="fb623-110">Tous les fournisseurs de services doivent écrire leur code afin qu’ils pour pouvoir compiler indépendamment ou non qu’ils prennent en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb623-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="fb623-111">Clients de compilation conditionnelle, en fonction de leur niveau de prise en charge, mais n’est pas le cas des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="fb623-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="fb623-112">Ils devront pas être recompilées lors de la modification du jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="fb623-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="fb623-113">Nothing dans le code de fournisseur de service doit être conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="fb623-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="fb623-114">Lorsque les clients ou fournisseurs de services qui prennent en charge Unicode émettre un appel de méthode qui inclut des chaînes de caractères en tant que paramètres d’entrée ou de sortie, ils définir l’indicateur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="fb623-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="fb623-115">Définition de cet indicateur indique à l’implémentation que toutes les chaînes entrants sont des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb623-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="fb623-116">Dans la sortie, définition de cet indicateur demandes que toutes les chaînes passées à partir de l’implémentation doit être chaînes Unicode si possible.</span><span class="sxs-lookup"><span data-stu-id="fb623-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="fb623-117">L’implémentation de méthode qui prennent en charge Unicode est conformes à la demande ; l’implémentation de méthode qui ne fournit pas de prise en charge Unicode n’est pas conforme.</span><span class="sxs-lookup"><span data-stu-id="fb623-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="fb623-118">Propriétés de type chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="fb623-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="fb623-119">MAPI définit la constante **fMapiUnicode** dans le fichier d’en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb623-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="fb623-120">Si un client ou fournisseur de services prend en charge Unicode, **fMapiUnicode** est définie sur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="fb623-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="fb623-121">Clients et fournisseurs de services qui ne prennent pas en charge Unicode **fMapiUnicode** la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fb623-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="fb623-122">Fournisseurs de services qui ne prennent pas en charge Unicode doivent :</span><span class="sxs-lookup"><span data-stu-id="fb623-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="fb623-123">Refuser effectuer des conversions entre les jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="fb623-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="fb623-124">L’indicateur MAPI_UNICODE jamais passer des appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="fb623-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="fb623-125">Retourner MAPI_E_BAD_CHARWIDTH lors de l’indicateur MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="fb623-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="fb623-126">Déclarer explicitement les propriétés de type chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb623-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="fb623-127">Fournisseurs de services peuvent également retourner MAPI_E_BAD_CHARWIDTH lorsqu’elles prennent uniquement en charge Unicode et les clients ne passent pas l’indicateur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="fb623-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="fb623-128">La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb623-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="fb623-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="fb623-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="fb623-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="fb623-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="fb623-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="fb623-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="fb623-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="fb623-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="fb623-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Implémentation**IAddrBook** uniquement)</span><span class="sxs-lookup"><span data-stu-id="fb623-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="fb623-134">Pour ces méthodes, les appelants peuvent s’attendre toutes les chaînes renvoyées à des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb623-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="fb623-135">Chaînes de caractères renvoyées à partir des implémentations MAPI de toute autre méthode seront des chaînes de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="fb623-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

