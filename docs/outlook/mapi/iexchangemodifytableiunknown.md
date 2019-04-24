---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350882"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="1d250-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d250-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="1d250-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d250-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d250-105">Prend en charge l'accès aux objets de tableau Microsoft Exchange Server, en particulier les objets de table de liste de contrôle d'accès système (SACL) et les objets de tableau de règles sur les dossiers Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1d250-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="1d250-106">Cette interface ressemble à l'interface [IMAPITable: IUnknown](imapitableiunknown.md) , mais elle ajoute la prise en charge des structures propres à Microsoft Exchange Server utilisées pour contrôler les listes SACL et les règles.</span><span class="sxs-lookup"><span data-stu-id="1d250-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d250-107">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="1d250-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="1d250-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="1d250-108">None</span></span>  <br/> |
|<span data-ttu-id="1d250-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1d250-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d250-110">Objets table de serveur</span><span class="sxs-lookup"><span data-stu-id="1d250-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="1d250-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1d250-111">Called by:</span></span>  <br/> |<span data-ttu-id="1d250-112">Applications MAPI et clientes</span><span class="sxs-lookup"><span data-stu-id="1d250-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="1d250-113">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="1d250-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1d250-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="1d250-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="1d250-115">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="1d250-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="1d250-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="1d250-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="1d250-117">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="1d250-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="1d250-118">Traitées</span><span class="sxs-lookup"><span data-stu-id="1d250-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1d250-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="1d250-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1d250-120">Généré</span><span class="sxs-lookup"><span data-stu-id="1d250-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="1d250-121">Renvoie des informations sur la dernière erreur qui s'est produite dans un objet table.</span><span class="sxs-lookup"><span data-stu-id="1d250-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="1d250-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="1d250-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="1d250-123">Renvoie un pointeur vers une interface pour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d250-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="1d250-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="1d250-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="1d250-125">Met à jour un objet table MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d250-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="1d250-126">**Propriétés utilisées pour modifier un tableau de règles**</span><span class="sxs-lookup"><span data-stu-id="1d250-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="1d250-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="1d250-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d250-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="1d250-148">**Propriétés utilisées pour modifier une table SACL**</span><span class="sxs-lookup"><span data-stu-id="1d250-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="1d250-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="1d250-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d250-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="1d250-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1d250-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d250-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1d250-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d250-158">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d250-158">Remarks</span></span>

<span data-ttu-id="1d250-159">Pour obtenir l'interface **IExchangeModifyTable** , appelez la méthode MAPI [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet Folder.</span><span class="sxs-lookup"><span data-stu-id="1d250-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="1d250-160">Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="1d250-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d250-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d250-161">See also</span></span>



[<span data-ttu-id="1d250-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1d250-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

