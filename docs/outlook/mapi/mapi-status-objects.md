---
title: Objets d'État MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309533"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="3a56e-103">Objets d'État MAPI</span><span class="sxs-lookup"><span data-stu-id="3a56e-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="3a56e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a56e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a56e-105">Les objets d'État indiquent des informations sur les ressources MAPI.</span><span class="sxs-lookup"><span data-stu-id="3a56e-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="3a56e-106">Par exemple, un fournisseur de services, le processus d'envoi/réception MAPI ou le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="3a56e-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="3a56e-107">Un objet d'État fournit des informations sur chaque fournisseur de services dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="3a56e-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="3a56e-108">MAPI est responsable de l'implémentation des objets d'État pour le sous-système, le processus d'envoi/réception MAPI et le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="3a56e-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="3a56e-109">L'objet état du sous-système fournit des informations globales.</span><span class="sxs-lookup"><span data-stu-id="3a56e-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="3a56e-110">L'objet Status du carnet d'adresses intégré fournit l'état de tous les fournisseurs de carnet d'adresses en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="3a56e-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="3a56e-111">Chaque objet Status est inclus dans le tableau d'État, une table gérée par MAPI qui fournit aux clients toutes les informations d'état de la session.</span><span class="sxs-lookup"><span data-stu-id="3a56e-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="3a56e-112">Pour plus d'informations, consultez la rubrique [tables d'État](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3a56e-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="3a56e-113">Les clients peuvent accéder à un objet d'état particulier via la table ou, pour un fournisseur de services, par le biais de son objet d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3a56e-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="3a56e-114">Par exemple, pour accéder à l'objet d'état d'un fournisseur de carnet d'adresses, un client peut appeler **IABLogon:: OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="3a56e-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="3a56e-115">Pour plus d'informations, voir [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="3a56e-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="3a56e-116">Les clients peuvent utiliser des objets d'État pour:</span><span class="sxs-lookup"><span data-stu-id="3a56e-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="3a56e-117">Découvrez l'état d'une session.</span><span class="sxs-lookup"><span data-stu-id="3a56e-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="3a56e-118">SurVeillez un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="3a56e-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="3a56e-119">Contrôler la transmission des messages.</span><span class="sxs-lookup"><span data-stu-id="3a56e-119">Control message transmission.</span></span>
    
- <span data-ttu-id="3a56e-120">Afficher ou modifier la configuration et l'état d'une ressource.</span><span class="sxs-lookup"><span data-stu-id="3a56e-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="3a56e-121">Chaque objet Status implémente l'interface **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="3a56e-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="3a56e-122">Pour plus d'informations, voir [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="3a56e-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="3a56e-123">Toutefois, tous les objets d'État ne prennent pas totalement en charge toutes les méthodes **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="3a56e-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="3a56e-124">Étant donné qu'il existe des variantes des méthodes prises en charge par un objet Status, les clients doivent en savoir plus sur un objet Status particulier avant de pouvoir l'utiliser.</span><span class="sxs-lookup"><span data-stu-id="3a56e-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="3a56e-125">Les objets d'État sont requis pour publier des informations sur leurs fonctionnalités dans les trois propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="3a56e-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="3a56e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a56e-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3a56e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a56e-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3a56e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3a56e-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="3a56e-129">Pour plus d'informations sur l'implémentation d'un objet [](status-object-implementation.md)Status, voir Status Implementation.</span><span class="sxs-lookup"><span data-stu-id="3a56e-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="3a56e-130">Pour plus d'informations sur l'utilisation d'un objet Status, consultez la rubrique [table d'État et objets d'État](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3a56e-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

