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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437531"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="79e6e-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79e6e-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="79e6e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79e6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79e6e-105">Fonctionne avec des fournisseurs de services dans un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79e6e-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79e6e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="79e6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="79e6e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79e6e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="79e6e-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="79e6e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="79e6e-109">Objets d’administration de fournisseur</span><span class="sxs-lookup"><span data-stu-id="79e6e-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="79e6e-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="79e6e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="79e6e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="79e6e-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="79e6e-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="79e6e-112">Called by:</span></span>  <br/> |<span data-ttu-id="79e6e-113">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="79e6e-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="79e6e-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="79e6e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="79e6e-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="79e6e-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="79e6e-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="79e6e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="79e6e-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="79e6e-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="79e6e-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="79e6e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="79e6e-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="79e6e-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="79e6e-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet d’administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="79e6e-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="79e6e-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="79e6e-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="79e6e-122">Permet d’accéder à la table des fournisseurs du service de messagerie, liste des fournisseurs de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79e6e-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="79e6e-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="79e6e-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="79e6e-124">Ajoute un fournisseur de services au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79e6e-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="79e6e-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="79e6e-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="79e6e-126">Supprime un fournisseur de services du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79e6e-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="79e6e-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="79e6e-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="79e6e-128">Ouvre une section de profil à partir du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="79e6e-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79e6e-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="79e6e-129">Remarks</span></span>

<span data-ttu-id="79e6e-130">Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Les fournisseurs de services sont transmis un pointeur **IProviderAdmin** lorsque la fonction de point d’entrée de leur service de messagerie est appelée.</span><span class="sxs-lookup"><span data-stu-id="79e6e-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79e6e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79e6e-131">See also</span></span>



[<span data-ttu-id="79e6e-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="79e6e-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

