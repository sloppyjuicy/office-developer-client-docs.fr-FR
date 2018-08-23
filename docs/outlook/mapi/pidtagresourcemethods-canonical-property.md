---
title: Propriété canonique PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578163"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="043b6-103">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="043b6-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="043b6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="043b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="043b6-105">Contient un masque binaire composé des indicateurs qui influencent les méthodes de l’interface **IMAPIStatus** qui sont prises en charge par l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="043b6-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="043b6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="043b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="043b6-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="043b6-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="043b6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="043b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="043b6-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="043b6-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="043b6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="043b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="043b6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="043b6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="043b6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="043b6-112">Area:</span></span>  <br/> |<span data-ttu-id="043b6-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="043b6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="043b6-114">Remarks</span></span>

<span data-ttu-id="043b6-115">Cette propriété indique parmi les méthodes de mise en œuvre d’un objet d’état de **IMAPIStatus** sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="043b6-116">Objets d’état sont autorisés à renvoyer MAPI_E_NO_SUPPORT à partir de méthodes non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="043b6-117">Clients utilisent état **PR_RESOURCE_METHODS** propriété d’un objet pour éviter d’effectuer des appels aux méthodes non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="043b6-118">Si l’indicateur qui correspond à une méthode particulière est défini, la méthode existe et peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="043b6-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="043b6-119">Si cet indicateur est désactivée, la méthode ne doit pas être appelée.</span><span class="sxs-lookup"><span data-stu-id="043b6-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="043b6-120">Les objets état implémentée par prise en charge MAPI les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="043b6-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="043b6-121">**Objet d’état**</span><span class="sxs-lookup"><span data-stu-id="043b6-121">**Status object**</span></span>|<span data-ttu-id="043b6-122">**Méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="043b6-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="043b6-123">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="043b6-124">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="043b6-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="043b6-125">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="043b6-126">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="043b6-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="043b6-127">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="043b6-128">**ValidateState** et **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="043b6-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="043b6-129">Un ou plusieurs des indicateurs suivants peuvent être définie dans **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="043b6-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="043b6-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="043b6-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="043b6-131">Indique que la méthode [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="043b6-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="043b6-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="043b6-133">Indique que la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="043b6-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="043b6-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="043b6-135">Indique que la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="043b6-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="043b6-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="043b6-137">Indique que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="043b6-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="043b6-138">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="043b6-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="043b6-139">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="043b6-139">Header files</span></span>

<span data-ttu-id="043b6-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="043b6-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="043b6-141">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="043b6-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="043b6-142">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="043b6-142">Mapitags.h</span></span>
  
> <span data-ttu-id="043b6-143">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="043b6-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="043b6-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="043b6-144">See also</span></span>



[<span data-ttu-id="043b6-145">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="043b6-146">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="043b6-147">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="043b6-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="043b6-148">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="043b6-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

