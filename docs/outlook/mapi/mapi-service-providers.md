---
title: Fournisseurs de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3f1cab24ef6bbd632ee3dc204e93f59e6f9ac846
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784712"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="62b3c-103">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="62b3c-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="62b3c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62b3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62b3c-105">Il existe trois principaux types de fournisseurs de services :</span><span class="sxs-lookup"><span data-stu-id="62b3c-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="62b3c-106">Fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="62b3c-106">Address book providers.</span></span>
    
- <span data-ttu-id="62b3c-107">Fournisseurs de magasins de message.</span><span class="sxs-lookup"><span data-stu-id="62b3c-107">Message store providers.</span></span>
    
- <span data-ttu-id="62b3c-108">Fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="62b3c-108">Transport providers.</span></span>
    
<span data-ttu-id="62b3c-109">Fournisseurs de magasin de messages et du carnet d’adresses présentent de nombreuses similitudes.</span><span class="sxs-lookup"><span data-stu-id="62b3c-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="62b3c-110">Ils inscrivent un identificateur unique MAPI qu’ils utilisent pour construire les identificateurs d’entrée pour leurs objets.</span><span class="sxs-lookup"><span data-stu-id="62b3c-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="62b3c-111">Elles fournissent une hiérarchie d’objets et que les clients peuvent accéder et manipuler les propriétés.</span><span class="sxs-lookup"><span data-stu-id="62b3c-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="62b3c-112">Pour les objets conteneur, elles prennent en charge une table de hiérarchie et une table des matières.</span><span class="sxs-lookup"><span data-stu-id="62b3c-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="62b3c-113">Elles prennent en charge les notifications sur ces tables et éventuellement sur des objets individuels afin que les clients peuvent être informés des modifications qui se produisent pendant la session.</span><span class="sxs-lookup"><span data-stu-id="62b3c-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="62b3c-114">Lorsque les opérations sont longues, ils peuvent afficher un indicateur de progression pour informer l’utilisateur de l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="62b3c-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="62b3c-115">Les clients peuvent communiquer avec des fournisseurs de banque de messages et du carnet d’adresse soit indirectement via MAPI à l’aide de la [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces ou directement à l’aide d’une des interfaces de fournisseur de service dans la tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="62b3c-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="62b3c-116">**Interfaces de fournisseur de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="62b3c-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="62b3c-117">**Interfaces de fournisseur de magasin de message**</span><span class="sxs-lookup"><span data-stu-id="62b3c-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62b3c-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="62b3c-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="62b3c-119">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62b3c-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="62b3c-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="62b3c-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="62b3c-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="62b3c-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="62b3c-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62b3c-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="62b3c-123">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62b3c-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="62b3c-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62b3c-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="62b3c-125">Fournisseurs de transport diffèrent auprès de fournisseurs de banque des messages et du carnet d’adresses de la façon de que communiquer avec MAPI et les clients.</span><span class="sxs-lookup"><span data-stu-id="62b3c-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="62b3c-126">Fournisseurs de transport attendre généralement MAPI pour demander les informations plutôt que d’établir une communication.</span><span class="sxs-lookup"><span data-stu-id="62b3c-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="62b3c-127">Contrairement aux autres fournisseurs, fournisseurs de transport ne prennent pas charge une variété de tables couramment utilisés par les clients et les objets.</span><span class="sxs-lookup"><span data-stu-id="62b3c-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="62b3c-128">Toutefois, elles prennent en charge un objet état, tous les fournisseurs de services, et publier ses propriétés dans la table d’état.</span><span class="sxs-lookup"><span data-stu-id="62b3c-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="62b3c-129">Tandis que les fournisseurs de magasins de messages et du carnet d’adresses appeler la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour enregistrer des identificateurs uniques pour construire les identificateurs d’entrée, fournisseurs de transport appellent la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) Enregistrez les identificateurs uniques, ainsi que les types d’adresses pour responsabilité pour la remise de messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="62b3c-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="62b3c-130">Votre fournisseur de services doit avoir les trois fichiers d’en-tête : un fichier d’en-tête public et deux fichiers internes.</span><span class="sxs-lookup"><span data-stu-id="62b3c-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="62b3c-131">Utilisez le fichier d’en-tête public pour la configuration et de la documentation des propriétés et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="62b3c-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="62b3c-132">Inclure dans un des fichiers d’en-tête interne tous les publics MAPI en-têtes nécessaires ; Ce fichier d’en-tête doit être inclus dans l’ensemble de vos fichiers source du fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="62b3c-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="62b3c-133">Utilisez l’autre fichier interne pour définir les identificateurs de ressource.</span><span class="sxs-lookup"><span data-stu-id="62b3c-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="62b3c-134">Carnet d’adresses, banque de messages et les fournisseurs de transport effectuent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="62b3c-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="62b3c-135">Fournir une fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="62b3c-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="62b3c-136">Fournir un fournisseur et un objet d’ouverture de session pour gérer l’ouverture de session et d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="62b3c-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="62b3c-137">Si le fournisseur appartient à un service de message, fournir une fonction de point d’entrée de message service.</span><span class="sxs-lookup"><span data-stu-id="62b3c-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="62b3c-138">Configuration de la prise en charge par l’implémentation d’une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="62b3c-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="62b3c-139">Mettre en œuvre un objet d’état et prise en charge de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="62b3c-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="62b3c-140">Poignée arrêtée.</span><span class="sxs-lookup"><span data-stu-id="62b3c-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62b3c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b3c-141">See also</span></span>



[<span data-ttu-id="62b3c-142">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="62b3c-142">MAPI Concepts</span></span>](mapi-concepts.md)

