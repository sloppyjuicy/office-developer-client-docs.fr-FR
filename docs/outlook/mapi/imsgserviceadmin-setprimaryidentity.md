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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784238"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="de415-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="de415-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="de415-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de415-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de415-105">Désigne un service de message pour être le fournisseur de l’identité principale pour le profil.</span><span class="sxs-lookup"><span data-stu-id="de415-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="de415-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de415-106">Parameters</span></span>

 <span data-ttu-id="de415-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="de415-107">_lpUID_</span></span>
  
> <span data-ttu-id="de415-108">[in] Un pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message fournir l’identité du principale, ou valeur NULL, ce qui indique que **SetPrimaryIdentity** doit effacer l’identité en cours.</span><span class="sxs-lookup"><span data-stu-id="de415-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="de415-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de415-109">_ulFlags_</span></span>
  
> <span data-ttu-id="de415-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="de415-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de415-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="de415-111">Return value</span></span>

<span data-ttu-id="de415-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="de415-112">S_OK</span></span> 
  
> <span data-ttu-id="de415-113">Le service de message a été correctement assigné le fournisseur de l’identité du principal.</span><span class="sxs-lookup"><span data-stu-id="de415-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="de415-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="de415-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="de415-115">**SetPrimaryIdentity** a tenté de désigner un service de message qui possède l’indicateur SERVICE_NO_PRIMARY_IDENTITY dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="de415-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de415-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="de415-116">Remarks</span></span>

<span data-ttu-id="de415-117">La méthode **IMsgServiceAdmin::SetPrimaryIdentity** établit un service de message en tant que le fournisseur de l’identité principale pour le profil.</span><span class="sxs-lookup"><span data-stu-id="de415-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="de415-118">L’identité du principale est généralement l’utilisateur qui est connecté au service de message.</span><span class="sxs-lookup"><span data-stu-id="de415-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="de415-119">Il est représenté par trois propriétés :</span><span class="sxs-lookup"><span data-stu-id="de415-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="de415-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de415-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="de415-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de415-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="de415-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de415-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="de415-123">Chaque fournisseur de service dans le service message désignés définit ces trois propriétés pour le nom complet, un identificateur d’entrée et une clé de recherche de l’utilisateur de messagerie qui fournit l’identité du principale.</span><span class="sxs-lookup"><span data-stu-id="de415-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="de415-124">Les clients peuvent récupérer identificateur d’entrée de l’identité principale en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="de415-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="de415-125">La propriété **PR_RESOURCE_FLAGS** est définie à STATUS_PRIMARY_IDENTITY pour chaque fournisseur qui est un membre du service de message qui fournit l’identité principale et SERVICE_PRIMARY_IDENTITY pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="de415-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="de415-126">Lorsqu’un fournisseur de services ne peut pas fournir l’identité du principale pour son service de message, il définit **PR_RESOURCE_FLAGS** STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="de415-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="de415-127">**SetPrimaryIdentity** définit la propriété **PR_RESOURCE_FLAGS** de chaque service de message qui ne fournit pas l’identité principale à SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="de415-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="de415-128">Chaque fournisseur de service de message MAPI dispose d’informations sur peut établir une identité pour chacun de ses utilisateurs lorsqu’un client se connecte au service.</span><span class="sxs-lookup"><span data-stu-id="de415-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="de415-129">Toutefois, MAPI prenant en charge les connexions à plusieurs fournisseurs de services pour chaque session MAPI, il n’existe aucune ferme définition de l’identité d’un utilisateur particulier pour la session MAPI dans sa globalité ; l’identité d’un utilisateur dépend du service qui est impliqué.</span><span class="sxs-lookup"><span data-stu-id="de415-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="de415-130">Les clients peuvent appeler **SetPrimaryIdentity** pour désigner l’une des nombreuses identités ouverte pour un utilisateur par les services de messagerie comme l’identité du principale de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="de415-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de415-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de415-131">See also</span></span>



[<span data-ttu-id="de415-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="de415-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="de415-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="de415-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="de415-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de415-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

