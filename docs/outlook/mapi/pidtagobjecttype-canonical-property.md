---
title: Propriété canonique PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329224"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="76295-103">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="76295-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="76295-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76295-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76295-105">Contient le type d’un objet.</span><span class="sxs-lookup"><span data-stu-id="76295-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76295-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="76295-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76295-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="76295-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="76295-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="76295-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76295-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="76295-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="76295-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="76295-110">Data type:</span></span>  <br/> |<span data-ttu-id="76295-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76295-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76295-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="76295-112">Area:</span></span>  <br/> |<span data-ttu-id="76295-113">Courant</span><span class="sxs-lookup"><span data-stu-id="76295-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76295-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="76295-114">Remarks</span></span>

<span data-ttu-id="76295-115">Le type d’objet contenu dans cette propriété correspond à l’interface principale disponible pour un objet accessible via l’interface **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="76295-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="76295-116">Elle est généralement obtenue en consultant le  _paramètre lpulObjType_ renvoyé par la méthode **OpenEntry** appropriée.</span><span class="sxs-lookup"><span data-stu-id="76295-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="76295-117">Lorsque l’interface est obtenue d’autres manières, appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="76295-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="76295-118">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="76295-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="76295-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="76295-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="76295-120">Objet conteneur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="76295-120">Address book container object</span></span> 
    
<span data-ttu-id="76295-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="76295-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="76295-122">Objet carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="76295-122">Address book object</span></span> 
    
<span data-ttu-id="76295-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="76295-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="76295-124">Objet de pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="76295-124">Message attachment object</span></span> 
    
<span data-ttu-id="76295-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="76295-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="76295-126">Objet de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="76295-126">Distribution list object</span></span> 
    
<span data-ttu-id="76295-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="76295-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="76295-128">Objet de dossier</span><span class="sxs-lookup"><span data-stu-id="76295-128">Folder object</span></span> 
    
<span data-ttu-id="76295-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="76295-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="76295-130">Objet Form</span><span class="sxs-lookup"><span data-stu-id="76295-130">Form object</span></span> 
    
<span data-ttu-id="76295-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="76295-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="76295-132">Objet utilisateur de messagerie</span><span class="sxs-lookup"><span data-stu-id="76295-132">Messaging user object</span></span> 
    
<span data-ttu-id="76295-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="76295-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="76295-134">Message, objet</span><span class="sxs-lookup"><span data-stu-id="76295-134">Message object</span></span> 
    
<span data-ttu-id="76295-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="76295-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="76295-136">Objet section profil</span><span class="sxs-lookup"><span data-stu-id="76295-136">Profile section object</span></span> 
    
<span data-ttu-id="76295-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="76295-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="76295-138">Objet Session</span><span class="sxs-lookup"><span data-stu-id="76295-138">Session object</span></span> 
    
<span data-ttu-id="76295-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="76295-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="76295-140">Objet Status</span><span class="sxs-lookup"><span data-stu-id="76295-140">Status object</span></span> 
    
<span data-ttu-id="76295-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="76295-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="76295-142">Objet de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="76295-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="76295-143">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="76295-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76295-144">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="76295-144">Protocol specifications</span></span>

<span data-ttu-id="76295-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-146">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="76295-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76295-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-148">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="76295-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="76295-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-150">Gère les communications d’un client avec un serveur NSPI (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="76295-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="76295-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-152">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="76295-152">Handles folder operations.</span></span>
    
<span data-ttu-id="76295-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-154">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="76295-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="76295-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-156">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="76295-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="76295-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-158">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="76295-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="76295-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-160">Spécifie les formats de fichier de carnet d’adresses en mode hors connexion pour le cache d’objets du carnet d’adresses local.</span><span class="sxs-lookup"><span data-stu-id="76295-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="76295-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-162">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="76295-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="76295-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76295-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76295-164">Spécifie les propriétés et les opérations de manipulation d’une configuration de liste de dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="76295-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76295-165">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="76295-165">Header files</span></span>

<span data-ttu-id="76295-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76295-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="76295-167">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="76295-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="76295-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76295-168">Mapitags.h</span></span>
  
> <span data-ttu-id="76295-169">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="76295-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76295-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76295-170">See also</span></span>



[<span data-ttu-id="76295-171">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="76295-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76295-172">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="76295-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76295-173">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="76295-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76295-174">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="76295-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

