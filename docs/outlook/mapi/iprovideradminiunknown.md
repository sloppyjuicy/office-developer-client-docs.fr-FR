---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784399"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="74c30-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74c30-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="74c30-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74c30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74c30-105">Fonctionne avec des fournisseurs de services dans un service de message.</span><span class="sxs-lookup"><span data-stu-id="74c30-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74c30-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="74c30-106">Header file:</span></span>  <br/> |<span data-ttu-id="74c30-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74c30-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="74c30-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="74c30-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="74c30-109">Objets d’administration fournisseur</span><span class="sxs-lookup"><span data-stu-id="74c30-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="74c30-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="74c30-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="74c30-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="74c30-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="74c30-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="74c30-112">Called by:</span></span>  <br/> |<span data-ttu-id="74c30-113">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="74c30-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="74c30-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="74c30-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="74c30-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="74c30-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="74c30-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="74c30-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="74c30-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="74c30-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="74c30-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="74c30-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="74c30-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="74c30-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="74c30-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite à l’objet de l’administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="74c30-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="74c30-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="74c30-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="74c30-122">Permet d’accéder à la table fournisseur du service de message, une liste des fournisseurs de services dans le service de message.</span><span class="sxs-lookup"><span data-stu-id="74c30-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="74c30-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="74c30-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="74c30-124">Ajoute un fournisseur de services pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="74c30-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="74c30-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="74c30-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="74c30-126">Supprime un fournisseur de services à partir du service de message.</span><span class="sxs-lookup"><span data-stu-id="74c30-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="74c30-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="74c30-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="74c30-128">Ouvre une section de profil du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="74c30-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74c30-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="74c30-129">Remarks</span></span>

<span data-ttu-id="74c30-130">Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; fournisseurs de services sont transmises un pointeur **IProviderAdmin** lors de la fonction de point d’entrée du service de leur message est appelée.</span><span class="sxs-lookup"><span data-stu-id="74c30-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74c30-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74c30-131">See also</span></span>



[<span data-ttu-id="74c30-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="74c30-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

