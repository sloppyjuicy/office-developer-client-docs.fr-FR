---
title: Fournisseurs de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409537"
---
# <a name="mapi-service-providers"></a><span data-ttu-id="dbf4f-103">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf4f-103">MAPI Service Providers</span></span>

  
  
<span data-ttu-id="dbf4f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbf4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbf4f-105">Il existe trois types courants de fournisseurs de services :</span><span class="sxs-lookup"><span data-stu-id="dbf4f-105">There are three common types of service providers:</span></span>
  
- <span data-ttu-id="dbf4f-106">Fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-106">Address book providers.</span></span>
    
- <span data-ttu-id="dbf4f-107">Fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-107">Message store providers.</span></span>
    
- <span data-ttu-id="dbf4f-108">Fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-108">Transport providers.</span></span>
    
<span data-ttu-id="dbf4f-109">Les fournisseurs de carnet d’adresses et de magasin de messages ont de nombreuses similitudes.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-109">Address book and message store providers have many similarities.</span></span> <span data-ttu-id="dbf4f-110">Ils enregistrent un identificateur unique auprès de MAPI qu’ils utilisent pour construire des identificateurs d’entrée pour leurs objets.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-110">They register a unique identifier with MAPI that they use for constructing entry identifiers for their objects.</span></span> <span data-ttu-id="dbf4f-111">Elles fournissent une hiérarchie d’objets et de propriétés accessibles et manipulées par les clients.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-111">They provide a hierarchy of objects and properties that clients can access and manipulate.</span></span> <span data-ttu-id="dbf4f-112">Pour leurs objets conteneur, ils supportent une table hiérarchique et une table des matières.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-112">For their container objects, they support a hierarchy table and a contents table.</span></span> <span data-ttu-id="dbf4f-113">Ils peuvent prendre en charge les notifications d’événement sur ces tables et éventuellement sur des objets individuels afin que les clients soient informés des modifications qui se produisent au cours de la session.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-113">They support event notification on these tables and optionally on individual objects so that clients can be informed of changes that occur during the session.</span></span> <span data-ttu-id="dbf4f-114">Lorsque les opérations deviennent longues, elles peuvent afficher un indicateur de progression pour informer l’utilisateur de l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-114">When operations become lengthy, they can display a progress indicator to inform the user of the operation's status.</span></span> <span data-ttu-id="dbf4f-115">Les clients peuvent communiquer avec les fournisseurs de carnet d’adresses et de magasin de messages indirectement via MAPI à l’aide de [l’IAddrBook : IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession : interfaces IUnknown](imapisessioniunknown.md) ou directement à l’aide de l’une des interfaces de fournisseur de services dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-115">Clients can communicate with address book and message store providers either indirectly through MAPI by using the [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) and [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces or directly by using one of the service provider interfaces in the following table.</span></span> 
  
|<span data-ttu-id="dbf4f-116">**Interfaces du fournisseur de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="dbf4f-116">**Address book provider interfaces**</span></span>|<span data-ttu-id="dbf4f-117">**Interfaces des fournisseurs de magasins de messages**</span><span class="sxs-lookup"><span data-stu-id="dbf4f-117">**Message store provider interfaces**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbf4f-118">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dbf4f-118">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md) <br/> |[<span data-ttu-id="dbf4f-119">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbf4f-119">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md) <br/> |
|[<span data-ttu-id="dbf4f-120">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dbf4f-120">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md) <br/> |[<span data-ttu-id="dbf4f-121">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dbf4f-121">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md) <br/> |
|[<span data-ttu-id="dbf4f-122">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbf4f-122">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md) <br/> |[<span data-ttu-id="dbf4f-123">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbf4f-123">IMessage : IMAPIProp</span></span>](imessageimapiprop.md) <br/> |
| <br/> |[<span data-ttu-id="dbf4f-124">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbf4f-124">IAttach : IMAPIProp</span></span>](iattachimapiprop.md) <br/> |
   
<span data-ttu-id="dbf4f-125">Les fournisseurs de transport diffèrent des fournisseurs de carnet d’adresses et de magasin de messages dans la façon dont ils communiquent avec MAPI et avec les clients.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-125">Transport providers differ from address book and message store providers in the way they communicate with MAPI and with clients.</span></span> <span data-ttu-id="dbf4f-126">Les fournisseurs de transport attendent généralement que MAPI les invite à fournir des informations plutôt que de lancer la communication.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-126">Transport providers typically wait for MAPI to prompt them for information rather than initiate communication.</span></span> <span data-ttu-id="dbf4f-127">Contrairement aux autres fournisseurs, les fournisseurs de transport ne sont pas en charge une variété d’objets et de tables couramment accessibles par les clients.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-127">Unlike the other providers, transport providers do not support a variety of objects and tables that are commonly accessed by clients.</span></span> <span data-ttu-id="dbf4f-128">Toutefois, ils ne prisent en charge un objet d’état, comme tous les fournisseurs de services, et publient ses propriétés dans le tableau d’état.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-128">However, they do support a status object, as do all service providers, and publish its properties in the status table.</span></span> <span data-ttu-id="dbf4f-129">Tandis que les fournisseurs de carnet d’adresses et de magasin de messages appellent la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire des identificateurs uniques pour la construction de leurs identificateurs d’entrée, les fournisseurs de transport appellent la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour inscrire des identificateurs uniques, ainsi que des types d’adresses pour assumer la responsabilité de la remise de messages particuliers.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-129">Whereas address book and message store providers call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register unique identifiers for constructing their entry identifiers, transport providers call the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to register unique identifiers, as well as address types for assuming responsibility for the delivery of particular messages.</span></span> 
  
<span data-ttu-id="dbf4f-130">Votre fournisseur de services doit avoir trois fichiers d’en-tête : un fichier d’en-tête public et deux fichiers internes.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-130">Your service provider should have three header files: one public header file and two internal files.</span></span> <span data-ttu-id="dbf4f-131">Utilisez le fichier d’en-tête public pour la configuration et la documentation des propriétés et de leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-131">Use the public header file for configuration and for documenting properties and their values.</span></span> <span data-ttu-id="dbf4f-132">Inclure dans l’un des fichiers d’en-tête internes tous les en-têtes MAPI publics nécessaires ; Ce fichier d’en-tête doit être inclus dans tous les fichiers sources de votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-132">Include in one of the internal header files all the necessary public MAPI headers; this header file should be included in all of your service provider source files.</span></span> <span data-ttu-id="dbf4f-133">Utilisez l’autre fichier interne pour définir les identificateurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-133">Use the other internal file to define resource identifiers.</span></span>
  
<span data-ttu-id="dbf4f-134">Les fournisseurs de carnet d’adresses, de magasin de messages et de transport effectuent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbf4f-134">Address book, message store, and transport providers perform the following tasks:</span></span>
  
- <span data-ttu-id="dbf4f-135">Fournir une fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-135">Supply an entry point function.</span></span> 
    
- <span data-ttu-id="dbf4f-136">Fournir un fournisseur et un objet d’personnalisation pour gérer l’personnalisation et l’personnalisation.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-136">Supply a provider and logon object to handle logon and initialization.</span></span> 
    
- <span data-ttu-id="dbf4f-137">Si le fournisseur appartient à un service de messagerie, fournissons une fonction de point d’entrée de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-137">If the provider belongs to a message service, supply a message service entry point function.</span></span> 
    
- <span data-ttu-id="dbf4f-138">Prise en charge de la configuration en implémentant une feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-138">Support configuration by implementing a property sheet.</span></span>
    
- <span data-ttu-id="dbf4f-139">Implémenter un objet d’état et la prise en charge de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-139">Implement a status object and support the status table.</span></span> 
    
- <span data-ttu-id="dbf4f-140">Gérer l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="dbf4f-140">Handle shut down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbf4f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbf4f-141">See also</span></span>



[<span data-ttu-id="dbf4f-142">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf4f-142">MAPI Concepts</span></span>](mapi-concepts.md)

