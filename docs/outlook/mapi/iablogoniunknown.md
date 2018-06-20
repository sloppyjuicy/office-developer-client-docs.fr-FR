---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783614"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="48c28-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48c28-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="48c28-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48c28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48c28-105">Ressources accède à un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="48c28-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48c28-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="48c28-106">Header file:</span></span>  <br/> |<span data-ttu-id="48c28-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="48c28-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="48c28-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="48c28-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="48c28-109">Objets d’ouverture de session de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="48c28-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="48c28-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="48c28-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="48c28-111">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="48c28-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="48c28-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="48c28-112">Called by:</span></span>  <br/> |<span data-ttu-id="48c28-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="48c28-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="48c28-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="48c28-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="48c28-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="48c28-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="48c28-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="48c28-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="48c28-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="48c28-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="48c28-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="48c28-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="48c28-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="48c28-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="48c28-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur livre adresse précédente.</span><span class="sxs-lookup"><span data-stu-id="48c28-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="48c28-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="48c28-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="48c28-122">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="48c28-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="48c28-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="48c28-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="48c28-124">Ouvre un conteneur, utilisateur ou les listes de distribution, de messagerie et retourne un pointeur vers une implémentation d’interface pour fournir un accès plus.</span><span class="sxs-lookup"><span data-stu-id="48c28-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="48c28-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="48c28-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="48c28-126">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="48c28-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="48c28-127">Conseiller</span><span class="sxs-lookup"><span data-stu-id="48c28-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="48c28-128">Enregistre l’appelant pour recevoir des notifications d’événements spécifiques qui affectent un conteneur, utilisateur ou liste de distribution de messagerie.</span><span class="sxs-lookup"><span data-stu-id="48c28-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="48c28-129">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="48c28-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="48c28-130">Annule les notifications qui ont été précédemment configurées avec un appel à la méthode **Advise** .</span><span class="sxs-lookup"><span data-stu-id="48c28-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="48c28-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="48c28-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="48c28-132">Ouvre l’objet d’état du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="48c28-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="48c28-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="48c28-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="48c28-134">Ouvre une entrée du destinataire qui comporte des données qui résident dans un fournisseur de carnet d’adresses hôte.</span><span class="sxs-lookup"><span data-stu-id="48c28-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="48c28-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="48c28-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="48c28-136">Renvoie un tableau des modèles uniques pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="48c28-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="48c28-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="48c28-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="48c28-138">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="48c28-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48c28-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="48c28-139">Remarks</span></span>

<span data-ttu-id="48c28-140">Pour obtenir des informations générales sur les méthodes de l’interface **IABLogon** , voir [L’implémentation de connexion au fournisseur de Service](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="48c28-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48c28-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48c28-141">See also</span></span>



[<span data-ttu-id="48c28-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="48c28-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

