---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408298"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="e4033-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e4033-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="e4033-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4033-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4033-105">Fournit des informations d'État sur le sous-système MAPI, le carnet d'adresses intégré et le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="e4033-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="e4033-106">Un fournisseur de services implémente **IMAPIStatus** pour fournir des informations sur son propre statut.</span><span class="sxs-lookup"><span data-stu-id="e4033-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4033-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e4033-107">Header file:</span></span>  <br/> |<span data-ttu-id="e4033-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e4033-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e4033-109">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="e4033-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e4033-110">Objets de statut</span><span class="sxs-lookup"><span data-stu-id="e4033-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="e4033-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e4033-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4033-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="e4033-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="e4033-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e4033-113">Called by:</span></span>  <br/> |<span data-ttu-id="e4033-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="e4033-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="e4033-115">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="e4033-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e4033-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="e4033-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="e4033-117">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="e4033-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e4033-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="e4033-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="e4033-119">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="e4033-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="e4033-120">Pas de transaction</span><span class="sxs-lookup"><span data-stu-id="e4033-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e4033-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="e4033-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e4033-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="e4033-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="e4033-123">Confirme les informations d'état externe disponibles pour la ressource MAPI ou le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e4033-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="e4033-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="e4033-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="e4033-125">Affiche une feuille de propriétés qui permet à l'utilisateur de modifier la configuration d'un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e4033-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="e4033-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="e4033-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="e4033-127">Modifie le mot de passe d'un fournisseur de services sans afficher d'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4033-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="e4033-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e4033-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="e4033-129">Force tous les messages en attente d'être envoyés ou reçus pour être immédiatement téléchargés ou téléchargés.</span><span class="sxs-lookup"><span data-stu-id="e4033-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="e4033-130">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="e4033-130">**Required properties**</span></span>|<span data-ttu-id="e4033-131">**Accès**</span><span class="sxs-lookup"><span data-stu-id="e4033-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4033-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e4033-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="e4033-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e4033-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="e4033-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4033-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="e4033-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4033-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="e4033-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4033-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="e4033-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4033-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="e4033-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e4033-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e4033-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4033-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4033-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4033-146">Remarks</span></span>

<span data-ttu-id="e4033-147">Les objets d'État que MAPI implémente prennent en charge les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="e4033-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="e4033-148">**Objet Status**</span><span class="sxs-lookup"><span data-stu-id="e4033-148">**Status object**</span></span>|<span data-ttu-id="e4033-149">**Méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="e4033-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4033-150">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="e4033-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="e4033-151">**ValidateState** uniquement</span><span class="sxs-lookup"><span data-stu-id="e4033-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="e4033-152">Carnet d'adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="e4033-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="e4033-153">**ValidateState** uniquement</span><span class="sxs-lookup"><span data-stu-id="e4033-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="e4033-154">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="e4033-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="e4033-155">**ValidateState** et **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="e4033-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="e4033-156">Les objets d'État implémentés par MAPI doivent disposer d'une version en lecture seule des méthodes de l'interface [IMAPIProp](imapipropiunknown.md) et prendre en charge la méthode **ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="e4033-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="e4033-157">Les fournisseurs de transport doivent également prendre en charge **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="e4033-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="e4033-158">Tous les fournisseurs doivent prendre en charge **SettingsDialog**; la prise en charge de **ChangePassword** est facultative.</span><span class="sxs-lookup"><span data-stu-id="e4033-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="e4033-159">Les clients utilisent les objets d'État pour effectuer la configuration et pour en savoir plus sur l'état de la session.</span><span class="sxs-lookup"><span data-stu-id="e4033-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="e4033-160">Ils accèdent à un objet état en appelant la méthode **OpenStatusEntry** d'un objet d'ouverture de session du fournisseur de services ou la méthode [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour extraire l'objet d'État.</span><span class="sxs-lookup"><span data-stu-id="e4033-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4033-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4033-161">See also</span></span>



[<span data-ttu-id="e4033-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e4033-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

