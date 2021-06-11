---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430363"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="4357b-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="4357b-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="4357b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4357b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4357b-105">Désigne un service de message comme fournisseur de l’identité principale du profil.</span><span class="sxs-lookup"><span data-stu-id="4357b-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="4357b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4357b-106">Parameters</span></span>

 <span data-ttu-id="4357b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="4357b-107">_lpUID_</span></span>
  
> <span data-ttu-id="4357b-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message pour fournir l’identité principale, ou NULL, qui indique que **SetPrimaryIdentity** doit effacer l’identité actuelle.</span><span class="sxs-lookup"><span data-stu-id="4357b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="4357b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4357b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4357b-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="4357b-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4357b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4357b-111">Return value</span></span>

<span data-ttu-id="4357b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4357b-112">S_OK</span></span> 
  
> <span data-ttu-id="4357b-113">Le service de message a été correctement affecté au fournisseur de l’identité principale.</span><span class="sxs-lookup"><span data-stu-id="4357b-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="4357b-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4357b-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4357b-115">**SetPrimaryIdentity** a tenté de désigner un service de message dont l’indicateur SERVICE_NO_PRIMARY_IDENTITY est PR_RESOURCE_FLAGS **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4357b-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4357b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4357b-116">Remarks</span></span>

<span data-ttu-id="4357b-117">La **méthode IMsgServiceAdmin::SetPrimaryIdentity** établit un service de message en tant que fournisseur de l’identité principale du profil.</span><span class="sxs-lookup"><span data-stu-id="4357b-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="4357b-118">L’identité principale est généralement l’utilisateur qui est connecté au service de message.</span><span class="sxs-lookup"><span data-stu-id="4357b-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="4357b-119">Il est représenté par trois propriétés :</span><span class="sxs-lookup"><span data-stu-id="4357b-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="4357b-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4357b-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="4357b-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4357b-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="4357b-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4357b-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="4357b-123">Chaque fournisseur de services dans le service de messagerie désigné définit ces trois propriétés sur le nom complet, l’identificateur d’entrée et la clé de recherche de l’utilisateur de messagerie qui fournit l’identité principale.</span><span class="sxs-lookup"><span data-stu-id="4357b-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="4357b-124">Les clients peuvent récupérer l’identificateur d’entrée de l’identité principale en appelant la méthode [IMAPISession::QueryIdentity.](imapisession-queryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="4357b-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="4357b-125">La **propriété PR_RESOURCE_FLAGS** est définie sur STATUS_PRIMARY_IDENTITY pour chaque fournisseur membre du service de messagerie qui fournit l’identité principale et sur SERVICE_PRIMARY_IDENTITY pour le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4357b-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="4357b-126">Lorsqu’un fournisseur de services ne peut pas fournir l’identité principale de son service de messagerie, il PR_RESOURCE_FLAGS **à** STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="4357b-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="4357b-127">**SetPrimaryIdentity** définit la **propriété PR_RESOURCE_FLAGS** de chaque service de message qui ne fournit pas l’identité principale à SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="4357b-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="4357b-128">Chaque fournisseur de services de messagerie dont MAPI dispose d’informations peut établir une identité pour chacun de ses utilisateurs lorsqu’un client se connecte au service.</span><span class="sxs-lookup"><span data-stu-id="4357b-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="4357b-129">Toutefois, étant donné que MAPI prend en charge les connexions à plusieurs fournisseurs de services pour chaque session MAPI, il n’existe aucune définition précise de l’identité d’un utilisateur particulier pour la session MAPI dans son ensemble ; L’identité d’un utilisateur dépend du service concerné.</span><span class="sxs-lookup"><span data-stu-id="4357b-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="4357b-130">Les clients peuvent appeler **SetPrimaryIdentity** pour désigner l’une des nombreuses identités établies pour un utilisateur par les services de message en tant qu’identité principale pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4357b-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4357b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4357b-131">See also</span></span>



[<span data-ttu-id="4357b-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="4357b-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="4357b-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4357b-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4357b-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4357b-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

