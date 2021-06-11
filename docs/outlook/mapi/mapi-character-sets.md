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
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417552"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="9e2ee-103">Jeux de caractères MAPI</span><span class="sxs-lookup"><span data-stu-id="9e2ee-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="9e2ee-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e2ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e2ee-105">Les applications clientes et les fournisseurs de services compatibles MAPI peuvent utiliser des caractères ANSI (un seul sur deux caractères) ou unicode (sur deux caractères).</span><span class="sxs-lookup"><span data-stu-id="9e2ee-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="9e2ee-106">Les jeux de caractères OEM ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-106">OEM character sets are not supported.</span></span> <span data-ttu-id="9e2ee-107">Une chaîne OEM transmise à une méthode ou une fonction MAPI entraîne l’échec de cette méthode ou fonction.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="9e2ee-108">Les applications clientes qui fonctionnent avec des noms de fichiers dans le jeu de caractères OEM doivent être attentives à les convertir en ANSI avant de les transmettre à une méthode ou une fonction MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="9e2ee-109">La prise en charge du jeu de caractères Unicode est facultative, à la fois pour les clients et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="9e2ee-110">Tous les fournisseurs de services doivent écrire leur code afin de pouvoir compiler, qu’ils soient ou non en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="9e2ee-111">Les clients sont compilés de manière conditionnable, en fonction de leur niveau de support, mais pas les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="9e2ee-112">Elles ne doivent pas être recompilées lorsque le jeu de caractères change.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="9e2ee-113">Rien dans le code du fournisseur de services ne doit être conditionnel.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="9e2ee-114">Lorsque des clients ou des fournisseurs de services qui supportent Unicode appellent une méthode qui inclut des chaînes de caractères en tant que paramètres d’entrée ou de sortie, ils définissent l’MAPI_UNICODE de sortie.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="9e2ee-115">La définition de cet indicateur indique à l’implémentation que toutes les chaînes entrantes sont des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="9e2ee-116">Lors de la sortie, la définition de cet indicateur demande que toutes les chaînes passées à partir de l’implémentation soient des chaînes Unicode si possible.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="9e2ee-117">Les implémenteurs de méthodes qui la prise en charge d’Unicode seront conformes à la demande ; les implémenteurs de méthode qui ne fournissent pas de prise en charge Unicode ne seront pas conformes.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="9e2ee-118">Les propriétés de chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="9e2ee-119">MAPI définit la constante **fMapiUnicode** dans le fichier d’en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="9e2ee-120">Si un client ou un fournisseur de services prend en charge Unicode, **fMapiUnicode** est MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="9e2ee-121">Les clients et les fournisseurs de services qui ne prisent pas en charge Unicode **définissent fMapiUnicode** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="9e2ee-122">Les fournisseurs de services qui ne prisent pas en charge Unicode doivent :</span><span class="sxs-lookup"><span data-stu-id="9e2ee-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="9e2ee-123">Refuser d’effectuer des conversions entre les jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="9e2ee-124">Ne passez jamais l’indicateur MAPI_UNICODE dans les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="9e2ee-125">Renvoyer MAPI_E_BAD_CHARWIDTH lorsque l’MAPI_UNICODE est transmis.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="9e2ee-126">Déclarez explicitement les propriétés de chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="9e2ee-127">Les fournisseurs de services peuvent également renvoyer MAPI_E_BAD_CHARWIDTH lorsqu’ils ne peuvent prendre en charge Unicode et que les clients ne passent pas l’indicateur MAPI_UNICODE’accès.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="9e2ee-128">La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e2ee-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="9e2ee-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="9e2ee-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="9e2ee-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="9e2ee-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="9e2ee-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="9e2ee-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="9e2ee-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="9e2ee-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="9e2ee-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**implémentation IAddrBook** uniquement)</span><span class="sxs-lookup"><span data-stu-id="9e2ee-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="9e2ee-134">Pour ces méthodes, les appelants peuvent s’attendre à ce que les chaînes renvoyées soient des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="9e2ee-135">Les chaînes de caractères renvoyées par les implémentations MAPI de toute autre méthode seront des chaînes de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e2ee-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

