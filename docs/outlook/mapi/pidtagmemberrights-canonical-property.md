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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397337"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="dc170-103">Propriété canonique PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="dc170-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="dc170-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc170-105">Contient un ensemble de bits indiquant les droits de ce membre sur un dossier ou d’une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="dc170-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc170-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dc170-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc170-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="dc170-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="dc170-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="dc170-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc170-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="dc170-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="dc170-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dc170-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc170-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc170-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc170-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dc170-112">Area:</span></span>  <br/> |<span data-ttu-id="dc170-113">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="dc170-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc170-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc170-114">Remarks</span></span>

<span data-ttu-id="dc170-115">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour définir les droits d’un membre d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="dc170-116">Ces droits peuvent être affichées et modifiées.</span><span class="sxs-lookup"><span data-stu-id="dc170-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="dc170-117">Les valeurs suivantes sont définies pour cette propriété de droits.</span><span class="sxs-lookup"><span data-stu-id="dc170-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="dc170-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="dc170-118">frightsReadAny</span></span>
  
> <span data-ttu-id="dc170-119">Membres peuvent lire tous les messages.</span><span class="sxs-lookup"><span data-stu-id="dc170-119">Member can read any messages.</span></span>
    
<span data-ttu-id="dc170-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="dc170-120">frightsCreate</span></span>
  
> <span data-ttu-id="dc170-121">Membre peut créer des messages.</span><span class="sxs-lookup"><span data-stu-id="dc170-121">Member can create messages.</span></span>
    
<span data-ttu-id="dc170-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="dc170-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="dc170-123">Membres peuvent modifier tous les messages appartenant à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc170-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="dc170-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="dc170-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="dc170-125">Membre peut supprimer tous les messages appartenant à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc170-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="dc170-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="dc170-126">frightsEditAny</span></span>
  
> <span data-ttu-id="dc170-127">Membres peuvent modifier tous les messages.</span><span class="sxs-lookup"><span data-stu-id="dc170-127">Member can edit any message.</span></span>
    
<span data-ttu-id="dc170-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="dc170-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="dc170-129">Membre peut supprimer tous les messages.</span><span class="sxs-lookup"><span data-stu-id="dc170-129">Member can delete any message.</span></span>
    
<span data-ttu-id="dc170-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="dc170-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="dc170-131">Membre peut créer des sous-dossiers du dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="dc170-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="dc170-132">frightsOwner</span></span>
  
> <span data-ttu-id="dc170-133">Membre a tous les droits précédents sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="dc170-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="dc170-134">frightsContact</span></span>
  
> <span data-ttu-id="dc170-135">Membre peut s’afficher votre nom en tant que contact dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="dc170-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="dc170-136">frightsVisible</span></span>
  
> <span data-ttu-id="dc170-137">Membre peut voir que le dossier existe.</span><span class="sxs-lookup"><span data-stu-id="dc170-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="dc170-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="dc170-138">rightsNone</span></span>
  
> <span data-ttu-id="dc170-139">Membre ne dispose pas des droits sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="dc170-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc170-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="dc170-141">Membre peut lire un message dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="dc170-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="dc170-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="dc170-143">Membres peuvent lire et écrire dans un message dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="dc170-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="dc170-144">rightsAll</span></span>
  
> <span data-ttu-id="dc170-145">Membre a tous les droits précédents sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="dc170-146">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dc170-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc170-147">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="dc170-147">Protocol specifications</span></span>

<span data-ttu-id="dc170-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc170-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc170-149">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="dc170-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc170-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc170-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc170-151">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="dc170-151">Handles folder operations.</span></span>
    
<span data-ttu-id="dc170-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc170-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc170-153">Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc170-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="dc170-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc170-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc170-155">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les éléments de calendrier et de message lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc170-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc170-156">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dc170-156">Header files</span></span>

<span data-ttu-id="dc170-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc170-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc170-158">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dc170-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc170-159">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="dc170-159">Mapitags.h</span></span>
  
> <span data-ttu-id="dc170-160">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="dc170-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc170-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc170-161">See also</span></span>



[<span data-ttu-id="dc170-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc170-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="dc170-163">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dc170-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc170-164">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dc170-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc170-165">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dc170-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc170-166">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dc170-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

