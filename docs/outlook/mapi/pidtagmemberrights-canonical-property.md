---
title: Propriété canonique PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342693"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="1a5a6-103">Propriété canonique PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="1a5a6-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="1a5a6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a5a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a5a6-105">Contient un ensemble de bits qui indiquent les droits de ce membre sur un dossier ou une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a5a6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1a5a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a5a6-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="1a5a6-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="1a5a6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1a5a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a5a6-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="1a5a6-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="1a5a6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1a5a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a5a6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a5a6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a5a6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1a5a6-112">Area:</span></span>  <br/> |<span data-ttu-id="1a5a6-113">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="1a5a6-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a5a6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a5a6-114">Remarks</span></span>

<span data-ttu-id="1a5a6-115">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour définir les droits d’un membre sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="1a5a6-116">Ces droits peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="1a5a6-117">Les valeurs suivantes sont des droits définis pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="1a5a6-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="1a5a6-118">frightsReadAny</span></span>
  
> <span data-ttu-id="1a5a6-119">Le membre peut lire n’importe quel message.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-119">Member can read any messages.</span></span>
    
<span data-ttu-id="1a5a6-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="1a5a6-120">frightsCreate</span></span>
  
> <span data-ttu-id="1a5a6-121">Le membre peut créer des messages.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-121">Member can create messages.</span></span>
    
<span data-ttu-id="1a5a6-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="1a5a6-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="1a5a6-123">Le membre peut modifier tous les messages de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="1a5a6-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="1a5a6-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="1a5a6-125">Le membre peut supprimer tous les messages de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="1a5a6-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="1a5a6-126">frightsEditAny</span></span>
  
> <span data-ttu-id="1a5a6-127">Le membre peut modifier n’importe quel message.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-127">Member can edit any message.</span></span>
    
<span data-ttu-id="1a5a6-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="1a5a6-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="1a5a6-129">Le membre peut supprimer n’importe quel message.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-129">Member can delete any message.</span></span>
    
<span data-ttu-id="1a5a6-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="1a5a6-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="1a5a6-131">Le membre peut créer des sous-dossiers pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="1a5a6-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="1a5a6-132">frightsOwner</span></span>
  
> <span data-ttu-id="1a5a6-133">Le membre dispose de tous les droits précédents sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="1a5a6-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="1a5a6-134">frightsContact</span></span>
  
> <span data-ttu-id="1a5a6-135">Le membre peut faire apparaître votre nom en tant que contact dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="1a5a6-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="1a5a6-136">frightsVisible</span></span>
  
> <span data-ttu-id="1a5a6-137">Le membre peut voir que le dossier existe.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="1a5a6-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="1a5a6-138">rightsNone</span></span>
  
> <span data-ttu-id="1a5a6-139">Le membre n’a pas de droits sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="1a5a6-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1a5a6-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="1a5a6-141">Le membre peut lire n’importe quel message dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="1a5a6-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a5a6-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="1a5a6-143">Le membre peut lire et écrire dans n’importe quel message du dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="1a5a6-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="1a5a6-144">rightsAll</span></span>
  
> <span data-ttu-id="1a5a6-145">Le membre dispose de tous les droits précédents sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1a5a6-146">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1a5a6-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a5a6-147">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1a5a6-147">Protocol specifications</span></span>

<span data-ttu-id="1a5a6-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a5a6-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a5a6-149">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a5a6-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a5a6-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a5a6-151">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-151">Handles folder operations.</span></span>
    
<span data-ttu-id="1a5a6-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a5a6-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a5a6-153">Gère la récupération des listes d’autorisations de dossier stockées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="1a5a6-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a5a6-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a5a6-155">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les éléments de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a5a6-156">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1a5a6-156">Header files</span></span>

<span data-ttu-id="1a5a6-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a5a6-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a5a6-158">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a5a6-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a5a6-159">Mapitags.h</span></span>
  
> <span data-ttu-id="1a5a6-160">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="1a5a6-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a5a6-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a5a6-161">See also</span></span>



[<span data-ttu-id="1a5a6-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a5a6-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="1a5a6-163">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1a5a6-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a5a6-164">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1a5a6-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a5a6-165">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1a5a6-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a5a6-166">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1a5a6-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

