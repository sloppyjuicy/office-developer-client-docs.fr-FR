---
title: Inscription des identificateurs uniques des fournisseurs de services
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
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="66bdd-103">Inscription des identificateurs uniques des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="66bdd-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="66bdd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66bdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66bdd-105">Le carnet d'adresses, la Banque de messages et les fournisseurs de transport utilisent un identificateur unique appelé [MAPIUID](mapiuid.md) pour s'inscrire aux objets de service de différents types.</span><span class="sxs-lookup"><span data-stu-id="66bdd-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="66bdd-106">Un **MAPIUID** est un identificateur de 16 octets qui contient un GUID.</span><span class="sxs-lookup"><span data-stu-id="66bdd-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="66bdd-107">Vous pouvez créer un **MAPIUID** à l'aide de la procédure suivante:</span><span class="sxs-lookup"><span data-stu-id="66bdd-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="66bdd-108">Définissez une constante.</span><span class="sxs-lookup"><span data-stu-id="66bdd-108">Define a constant.</span></span>
    
2. <span data-ttu-id="66bdd-109">Appelez l'outil de*création de GUID*\* Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="66bdd-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="66bdd-110">Par exemple, un fournisseur de carnet d'adresses peut inclure la constante suivante dans un fichier d'en-tête pour définir un **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="66bdd-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="66bdd-111">**Pour enregistrer un MAPIUID si votre fournisseur est un carnet d'adresses ou un fournisseur de banque de messages**</span><span class="sxs-lookup"><span data-stu-id="66bdd-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="66bdd-112">Appelez [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="66bdd-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="66bdd-113">Inscrivez un **MAPIUID** pour chaque objet d'ouverture de session que vous instanciez et incluez cette **MAPIUID** dans les 16 premiers octets du membre **AB** de chaque identificateur d'entrée que vous créez.</span><span class="sxs-lookup"><span data-stu-id="66bdd-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="66bdd-114">MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="66bdd-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="66bdd-115">Lorsqu'un client appelle la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l'identificateur d'entrée, en la comparant à la **MAPIUID**enregistrée, afin de déterminer l'objet d'ouverture de session qui doit recevoir l'élément Open. sollicit.</span><span class="sxs-lookup"><span data-stu-id="66bdd-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="66bdd-116">Si votre fournisseur est un transport, enregistrez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre méthode **IXPLogon:: AddressTypes** .</span><span class="sxs-lookup"><span data-stu-id="66bdd-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="66bdd-117">MAPI utilise les structures **MAPIUID** enregistrées par les fournisseurs de transport pour affecter la responsabilité de la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="66bdd-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="66bdd-118">Bien que les fournisseurs de services inscrivent généralement un seul **MAPIUID**, vous pouvez enregistrer plusieurs structures **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="66bdd-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="66bdd-119">Si votre carnet d'adresses ou votre fournisseur de banque de messages prend en charge plusieurs objets d'ouverture de session, par exemple, en permettant à un utilisateur d'ajouter plusieurs instances de votre fournisseur à son profil, vous pouvez implémenter un autre **MAPIUID** pour chaque objet d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="66bdd-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="66bdd-120">Il existe d'autres raisons de prendre en charge plusieurs **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="66bdd-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="66bdd-121">Vous devez prendre en charge plusieurs versions de votre fournisseur et les identificateurs d'entrée doivent représenter la version appropriée.</span><span class="sxs-lookup"><span data-stu-id="66bdd-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="66bdd-122">Affectez une autre **MAPIUID** pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="66bdd-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="66bdd-123">Vous souhaitez faire la distinction entre les types d'objets que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="66bdd-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="66bdd-124">Par exemple, un fournisseur de carnet d'adresses peut souhaiter enregistrer un **MAPIUID** à utiliser dans les identificateurs d'entrée de ses objets utilisateur de messagerie et un autre **MAPIUID** à utiliser pour les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="66bdd-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="66bdd-125">Lorsque plusieurs objets d'ouverture de session sont actifs simultanément, il est logique d'avoir des structures **MAPIUID** uniques pour chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="66bdd-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="66bdd-126">Cela augmente la précision avec laquelle MAPI établit une correspondance entre les identificateurs d'entrée et les fournisseurs de services et enregistre le travail.</span><span class="sxs-lookup"><span data-stu-id="66bdd-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="66bdd-127">Lorsque chaque objet Logon a son propre identificateur unique, MAPI peut garantir que toute requête qu'il dirige vers un objet Logon peut être gérée par cet objet.</span><span class="sxs-lookup"><span data-stu-id="66bdd-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="66bdd-128">Lorsque les objets d'ouverture de session partagent des structures **MAPIUID** , MAPI achemine la demande vers le premier objet ouverture de session qui est identifié par l' **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="66bdd-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="66bdd-129">Si l'un de vos objets d'ouverture de session reçoit une demande qu'il ne peut pas traiter, car il ne gère pas l'identificateur d'entrée, transmettez la demande à votre prochain objet d'ouverture de session avant de renvoyer une erreur.</span><span class="sxs-lookup"><span data-stu-id="66bdd-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66bdd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66bdd-130">See also</span></span>



[<span data-ttu-id="66bdd-131">Implémentation de la connexion au fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="66bdd-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

