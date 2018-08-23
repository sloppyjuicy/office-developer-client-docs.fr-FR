---
title: Objets d’état MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 69a4d25fc6a7abec68c94cc947e5944322d230a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594949"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="b2337-103">Objets d’état MAPI</span><span class="sxs-lookup"><span data-stu-id="b2337-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="b2337-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2337-105">Objets d’état signalent des informations sur les ressources MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2337-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="b2337-106">Par exemple, un fournisseur de services, le processus d’envoi/réception MAPI ou le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b2337-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="b2337-107">Il existe un objet de l’état en fournissant des informations sur chaque fournisseur de services individuels dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="b2337-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="b2337-108">MAPI est responsable de l’implémentation d’objets d’état pour le carnet d’adresses, le processus d’envoi/réception MAPI et du sous-système.</span><span class="sxs-lookup"><span data-stu-id="b2337-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="b2337-109">L’objet de l’état du sous-système fournit des informations globales.</span><span class="sxs-lookup"><span data-stu-id="b2337-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="b2337-110">L’objet d’état pour le carnet d’adresses intégré fournit l’état de tous les fournisseurs de carnet d’adresses en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b2337-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="b2337-111">Chaque objet de l’état est inclus dans la table d’état, une table gérée par MAPI qui fournit aux clients avec toutes les informations d’état de la session.</span><span class="sxs-lookup"><span data-stu-id="b2337-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="b2337-112">Pour plus d’informations, voir [Tableaux d’état](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b2337-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="b2337-113">Clients peuvent accéder à un objet d’état spécifique par le biais de la table ou, pour un fournisseur de service, par le biais de son objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b2337-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="b2337-114">Par exemple, pour accéder aux objets de l’état d’un fournisseur de carnet d’adresses, un client peut appeler **IABLogon::OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="b2337-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="b2337-115">Pour plus d’informations, voir [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="b2337-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="b2337-116">Clients peuvent utiliser les objets d’état :</span><span class="sxs-lookup"><span data-stu-id="b2337-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="b2337-117">Obtenir des informations sur l’état d’une session.</span><span class="sxs-lookup"><span data-stu-id="b2337-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="b2337-118">Surveiller un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b2337-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="b2337-119">Contrôle la transmission des messages.</span><span class="sxs-lookup"><span data-stu-id="b2337-119">Control message transmission.</span></span>
    
- <span data-ttu-id="b2337-120">Afficher ou modifier la configuration et l’état d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="b2337-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="b2337-121">Chaque objet état implémente l’interface **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="b2337-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="b2337-122">Pour plus d’informations, voir [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b2337-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="b2337-123">Toutefois, non à chaque objet état prend entièrement en charge chaque méthode **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="b2337-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="b2337-124">Étant donné que les variantes dans les méthodes qui sont pris en charge par un objet d’état, les clients ont besoin pour en savoir plus sur un objet d’état spécifique avant de pouvoir l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b2337-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="b2337-125">Objets d’état sont requises pour publier des informations sur les fonctionnalités dans les trois propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2337-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="b2337-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2337-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="b2337-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2337-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="b2337-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b2337-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="b2337-129">Pour plus d’informations sur l’implémentation d’un objet d’état, voir [Implémentation d’objet état](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b2337-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="b2337-130">Pour plus d’informations sur l’utilisation d’un objet d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b2337-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

