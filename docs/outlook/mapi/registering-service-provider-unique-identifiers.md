---
title: Inscription des identificateurs uniques du fournisseur de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410174"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="7b202-103">Inscription des identificateurs uniques du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="7b202-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="7b202-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b202-105">Les fournisseurs de carnet d’adresses, de magasin de messages et de transport utilisent un identificateur unique appelé [MAPIUID](mapiuid.md) pour s’inscrire aux objets de service de différents types.</span><span class="sxs-lookup"><span data-stu-id="7b202-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="7b202-106">**MapIUID est** un identificateur de 16 byte qui contient un GUID.</span><span class="sxs-lookup"><span data-stu-id="7b202-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="7b202-107">Vous pouvez créer un **MAPIUID** à l’aide de la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="7b202-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="7b202-108">Définissez une constante.</span><span class="sxs-lookup"><span data-stu-id="7b202-108">Define a constant.</span></span>
    
2. <span data-ttu-id="7b202-109">Invoke the Visual Studio *Create GUID*\* tool.</span><span class="sxs-lookup"><span data-stu-id="7b202-109">Invoke the Visual Studio *Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="7b202-110">Par exemple, un fournisseur de carnet d’adresses peut inclure la constante suivante dans un fichier d’en-tête pour définir un **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="7b202-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="7b202-111">**Pour inscrire un MAPIUID si votre fournisseur est un fournisseur de carnet d’adresses ou de magasin de messages**</span><span class="sxs-lookup"><span data-stu-id="7b202-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="7b202-112">Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="7b202-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="7b202-113">Inscrivez un **MAPIUID** pour chaque objet d’inscription que vous inséziez et incluez ce **MAPIUID** dans les 16 premiers octets du membre **ab** de chaque identificateur d’entrée que vous créez.</span><span class="sxs-lookup"><span data-stu-id="7b202-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="7b202-114">MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="7b202-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="7b202-115">Lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l’identificateur d’entrée, en la faisant correspondre à l’identificateur **MAPIUID** enregistré, pour déterminer quel objet d’ouverture doit recevoir la demande d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="7b202-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="7b202-116">Si votre fournisseur est un transport, inscrivez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre **méthode IXPLogon::AddressTypes.**</span><span class="sxs-lookup"><span data-stu-id="7b202-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="7b202-117">MAPI utilise les structures **MAPIUID** enregistrées par les fournisseurs de transport pour attribuer la responsabilité de la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="7b202-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="7b202-118">Bien que les fournisseurs de services enregistrent généralement un **seul MAPIUID,** vous pouvez inscrire plusieurs structures **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="7b202-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="7b202-119">Si votre carnet d’adresses ou votre fournisseur de magasins de messages prend en charge plusieurs objets d’ouverture de page, par exemple en permettant à un utilisateur d’ajouter plusieurs instances de votre fournisseur à son profil, vous pouvez implémenter un **MAPIUID** différent pour chaque objet d’ouverture de page.</span><span class="sxs-lookup"><span data-stu-id="7b202-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="7b202-120">Il existe quelques autres raisons de prendre en charge plusieurs **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="7b202-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="7b202-121">Vous devez prendre en charge plusieurs versions de votre fournisseur et les identificateurs d’entrée doivent représenter la version appropriée.</span><span class="sxs-lookup"><span data-stu-id="7b202-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="7b202-122">Affectez un **MAPIUID différent** pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="7b202-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="7b202-123">Vous souhaitez faire la distinction entre les types d’objets que vous prendrez en charge.</span><span class="sxs-lookup"><span data-stu-id="7b202-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="7b202-124">Par exemple, un fournisseur de carnet d’adresses peut inscrire un **MAPIUID** à utiliser dans les identificateurs d’entrée de ses objets utilisateur de messagerie et un **autre MAPIUID** à utiliser pour les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="7b202-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="7b202-125">Lorsqu’il existe plusieurs objets de session qui sont actifs simultanément, il est logique d’avoir des structures **MAPIUID** uniques pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="7b202-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="7b202-126">Cela augmente la précision avec laquelle MAPI fait la correspondance entre les identificateurs d’entrée et les fournisseurs de services et enregistre du travail.</span><span class="sxs-lookup"><span data-stu-id="7b202-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="7b202-127">Lorsque chaque objet d' logon possède son propre identificateur unique, MAPI peut garantir que toute demande qu’il a route vers un objet d’logon peut être gérée par cet objet.</span><span class="sxs-lookup"><span data-stu-id="7b202-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="7b202-128">Lorsque des objets d' logon partagent des structures **MAPIUID,** MAPI a pour effet d’approvisionnement la demande vers le premier objet d' logon qui est identifié par **mapIUID**.</span><span class="sxs-lookup"><span data-stu-id="7b202-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="7b202-129">Si l’un de vos objets d’inscription reçoit une demande qu’il ne peut pas traiter car elle ne gère pas l’identificateur d’entrée, passez la demande à votre prochain objet d’inscription avant de renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7b202-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b202-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b202-130">See also</span></span>



[<span data-ttu-id="7b202-131">Mise en œuvre de l’logo du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="7b202-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

