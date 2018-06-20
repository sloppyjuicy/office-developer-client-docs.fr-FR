---
title: Inscription des identificateurs uniques de fournisseur de Service
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786983"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="b1343-103">Inscription des identificateurs uniques de fournisseur de Service</span><span class="sxs-lookup"><span data-stu-id="b1343-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="b1343-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1343-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1343-105">Carnet d’adresses, banque de messages et les fournisseurs de transport permet d’un identificateur unique, appelé un [MAPIUID](mapiuid.md) pour enregistrer aux objets de différents types de service.</span><span class="sxs-lookup"><span data-stu-id="b1343-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="b1343-106">Un **MAPIUID** est un identificateur de 16 octets qui contient un GUID.</span><span class="sxs-lookup"><span data-stu-id="b1343-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="b1343-107">Vous pouvez créer un **MAPIUID** à l’aide de la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="b1343-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="b1343-108">Définir une constante.</span><span class="sxs-lookup"><span data-stu-id="b1343-108">Define a constant.</span></span>
    
2. <span data-ttu-id="b1343-109">Appeler le Visual Studio*Create GUID*\* outil.</span><span class="sxs-lookup"><span data-stu-id="b1343-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="b1343-110">Par exemple, un fournisseur de carnet d’adresses peut inclure la constante suivante dans un fichier d’en-tête pour définir un **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="b1343-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="b1343-111">**Pour inscrire un MAPIUID si votre fournisseur est un fournisseur de magasin de message ou de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="b1343-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="b1343-112">Appelez [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="b1343-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="b1343-113">Inscrire un **MAPIUID** pour chaque ouverture de session d’objet que vous instanciez et incluez ce **MAPIUID** dans les premier 16 octets du membre **ab** de chaque identificateur d’entrée que vous créez.</span><span class="sxs-lookup"><span data-stu-id="b1343-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="b1343-114">MAPI utilise des structures **MAPIUID** pour associer des objets à des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="b1343-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="b1343-115">Lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un objet, MAPI examine la partie **MAPIUID** de l’identificateur d’entrée, l’associer à l’inscrits **MAPIUID**, pour déterminer l’objet d’ouverture de session doit recevoir l’ouvrir demande.</span><span class="sxs-lookup"><span data-stu-id="b1343-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="b1343-116">Si votre fournisseur est un type de transport, enregistrez une ou plusieurs structures **MAPIUID** lorsque MAPI appelle votre méthode **IXPLogon::AddressTypes** .</span><span class="sxs-lookup"><span data-stu-id="b1343-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="b1343-117">MAPI utilise les structures **MAPIUID** enregistrés par des fournisseurs de transport pour affecter la responsabilité de la remise du message.</span><span class="sxs-lookup"><span data-stu-id="b1343-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="b1343-118">Bien que les fournisseurs de services généralement enregistrement un seul **MAPIUID**, vous pouvez inscrire plusieurs structures **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="b1343-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="b1343-119">Si votre carnet d’adresses ou un message magasins fournisseur prend en charge plusieurs objets de l’ouverture de session, peut-être en permettant à un utilisateur pour ajouter plusieurs instances de votre fournisseur à leur profil, vous souhaitez implémenter une autre **MAPIUID** pour chaque objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b1343-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="b1343-120">Il existe quelques autres raisons pour prendre en charge de plusieurs **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="b1343-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="b1343-121">À prendre en charge plusieurs versions de votre fournisseur et les identificateurs d’entrée doivent représenter la version appropriée.</span><span class="sxs-lookup"><span data-stu-id="b1343-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="b1343-122">Affecter un autre **MAPIUID** pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="b1343-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="b1343-123">Vous souhaitez faire la distinction entre les types d’objets que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="b1343-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="b1343-124">Par exemple, un fournisseur de carnet d’adresses souhaiterez inscrire un **MAPIUID** à utiliser dans les identificateurs d’entrée de ses objets utilisateur de messagerie et un autre **MAPIUID** à utiliser pour les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="b1343-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="b1343-125">Lorsqu’il existe plusieurs objets d’ouverture de session qui sont actifs simultanément, il est judicieux ont des structures **MAPIUID** uniques pour chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="b1343-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="b1343-126">Cela permet d’augmenter la précision qui établit une correspondance avec les identificateurs d’entrée aux fournisseurs de services MAPI et enregistre un travail.</span><span class="sxs-lookup"><span data-stu-id="b1343-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="b1343-127">Lorsque tous les objets d’ouverture de session a son propre identificateur unique, MAPI peut garantir que toute demande elle dirige vers un objet d’ouverture de session peut être gérés par l’objet.</span><span class="sxs-lookup"><span data-stu-id="b1343-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="b1343-128">Lorsque vous partagez des structures **MAPIUID** objets d’ouverture de session, MAPI achemine la demande au premier objet identifié par l' **MAPIUID**d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b1343-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="b1343-129">Si un de vos objets d’ouverture de session reçoit une demande qu’il ne peut pas traiter, car il ne gère pas l’identificateur d’entrée, transmettez la demande à votre objet d’ouverture de session suivant avant qu’une erreur.</span><span class="sxs-lookup"><span data-stu-id="b1343-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1343-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1343-130">See also</span></span>



[<span data-ttu-id="b1343-131">L’implémentation du fournisseur de Service d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="b1343-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

