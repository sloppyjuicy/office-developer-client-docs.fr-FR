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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431077"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="c8c28-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8c28-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="c8c28-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8c28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8c28-105">Accède aux ressources d'un fournisseur de carnets d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c8c28-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8c28-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c8c28-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8c28-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="c8c28-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="c8c28-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="c8c28-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c8c28-109">Objets d'ouverture de session du carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="c8c28-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="c8c28-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c8c28-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8c28-111">Fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="c8c28-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="c8c28-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c8c28-112">Called by:</span></span>  <br/> |<span data-ttu-id="c8c28-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8c28-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8c28-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="c8c28-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c8c28-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="c8c28-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="c8c28-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="c8c28-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c8c28-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="c8c28-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c8c28-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="c8c28-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c8c28-119">Généré</span><span class="sxs-lookup"><span data-stu-id="c8c28-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="c8c28-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur du fournisseur de carnet d'adresses précédent.</span><span class="sxs-lookup"><span data-stu-id="c8c28-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="c8c28-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="c8c28-122">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="c8c28-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c8c28-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="c8c28-124">Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution, et renvoie un pointeur vers une implémentation d'interface pour fournir un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c8c28-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c8c28-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="c8c28-126">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="c8c28-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-127">Recommander</span><span class="sxs-lookup"><span data-stu-id="c8c28-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="c8c28-128">Inscrit l'appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="c8c28-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="c8c28-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="c8c28-130">Annule les notifications précédemment configurées avec un appel à la \*\*\*\* méthode Advise.</span><span class="sxs-lookup"><span data-stu-id="c8c28-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="c8c28-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="c8c28-132">Ouvre l'objet d'État du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c8c28-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="c8c28-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="c8c28-134">Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d'adresses hôte.</span><span class="sxs-lookup"><span data-stu-id="c8c28-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="c8c28-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="c8c28-136">Renvoie une table des modèles uniques permettant de créer des destinataires à ajouter à la liste des destinataires d'un message sortant.</span><span class="sxs-lookup"><span data-stu-id="c8c28-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="c8c28-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="c8c28-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="c8c28-138">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8c28-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8c28-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8c28-139">Remarks</span></span>

<span data-ttu-id="c8c28-140">Pour obtenir des informations générales sur les méthodes de l'interface **IABLogon** , consultez la rubrique [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="c8c28-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8c28-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8c28-141">See also</span></span>



[<span data-ttu-id="c8c28-142">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c8c28-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

