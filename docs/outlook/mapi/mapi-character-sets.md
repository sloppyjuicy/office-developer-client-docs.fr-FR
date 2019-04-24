---
title: Jeux de caractères MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319074"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="042a5-103">Jeux de caractères MAPI</span><span class="sxs-lookup"><span data-stu-id="042a5-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="042a5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="042a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="042a5-105">Les fournisseurs de services et les applications clientes conformes à la norme MAPI peuvent utiliser des caractères ANSI (codés sur un octet) ou Unicode (double octet).</span><span class="sxs-lookup"><span data-stu-id="042a5-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="042a5-106">Les jeux de caractères OEM ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="042a5-106">OEM character sets are not supported.</span></span> <span data-ttu-id="042a5-107">Une chaîne OEM transmise à une méthode ou à une fonction MAPI entraîne l'échec de cette méthode ou fonction.</span><span class="sxs-lookup"><span data-stu-id="042a5-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="042a5-108">Les applications clientes qui fonctionnent avec des noms de fichier dans le jeu de caractères OEM doivent être converties en ANSI avant de les transmettre à une méthode ou à une fonction MAPI.</span><span class="sxs-lookup"><span data-stu-id="042a5-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="042a5-109">La prise en charge du jeu de caractères Unicode est facultative pour les clients et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="042a5-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="042a5-110">Tous les fournisseurs de services doivent écrire leur code afin qu'ils puissent effectuer une compilation, qu'ils prennent ou non en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="042a5-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="042a5-111">Les clients sont compilés de manière conditionnelle, en fonction de leur niveau de prise en charge, mais pas des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="042a5-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="042a5-112">Elles ne doivent pas être recompilées lorsque le jeu de caractères est modifié.</span><span class="sxs-lookup"><span data-stu-id="042a5-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="042a5-113">Nothing dans le code du fournisseur de services doit être conditionnel.</span><span class="sxs-lookup"><span data-stu-id="042a5-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="042a5-114">Lorsque des clients ou des fournisseurs de services qui prennent en charge Unicode effectuent un appel de méthode qui inclut des chaînes de caractères comme paramètres d'entrée ou de sortie, ils définissent l'indicateur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="042a5-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="042a5-115">La définition de cet indicateur indique à l'implémentation que toutes les chaînes entrantes sont des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="042a5-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="042a5-116">Lors de la sortie, la définition de cet indicateur demande que toutes les chaînes transmises à partir de l'implémentation soient des chaînes Unicode dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="042a5-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="042a5-117">Les implémenteurs de méthode qui prennent en charge Unicode seront conformes à la demande; les implémenteurs de méthodes qui ne fournissent pas de prise en charge d'Unicode ne seront pas conformes.</span><span class="sxs-lookup"><span data-stu-id="042a5-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="042a5-118">Les propriétés de chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="042a5-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="042a5-119">MAPI définit la constante **fMapiUnicode** dans le fichier d'en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="042a5-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="042a5-120">Si un client ou un fournisseur de services prend en charge Unicode, **fMapiUnicode** est défini sur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="042a5-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="042a5-121">Les clients et fournisseurs de services qui ne prennent pas en charge Unicode Set **fMapiUnicode** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="042a5-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="042a5-122">Les fournisseurs de services qui ne prennent pas en charge Unicode doivent:</span><span class="sxs-lookup"><span data-stu-id="042a5-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="042a5-123">Refuser d'effectuer des conversions entre des jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="042a5-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="042a5-124">Ne transmettez jamais l'indicateur MAPI_UNICODE dans les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="042a5-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="042a5-125">Renvoie MAPI_E_BAD_CHARWIDTH lorsque l'indicateur MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="042a5-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="042a5-126">Déclarez explicitement les propriétés de chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="042a5-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="042a5-127">Les fournisseurs de services peuvent également renvoyer MAPI_E_BAD_CHARWIDTH lorsqu'ils prennent en charge uniquement Unicode et que les clients ne passent pas l'indicateur MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="042a5-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="042a5-128">La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="042a5-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="042a5-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="042a5-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="042a5-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="042a5-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="042a5-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="042a5-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="042a5-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="042a5-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="042a5-133">[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Implémentation**IAddrBook** uniquement)</span><span class="sxs-lookup"><span data-stu-id="042a5-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="042a5-134">Pour ces méthodes, les appelants peuvent s'attendre à ce que toutes les chaînes renvoyées soient des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="042a5-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="042a5-135">Les chaînes de caractères renvoyées par les implémentations MAPI de n'importe quelle autre méthode sont des chaînes de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="042a5-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

