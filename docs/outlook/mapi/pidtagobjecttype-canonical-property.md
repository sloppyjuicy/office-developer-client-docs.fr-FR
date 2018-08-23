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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591050"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="8d084-103">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="8d084-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="8d084-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d084-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d084-105">Contient le type d’un objet.</span><span class="sxs-lookup"><span data-stu-id="8d084-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d084-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8d084-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d084-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="8d084-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="8d084-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8d084-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d084-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="8d084-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="8d084-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8d084-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d084-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d084-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d084-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8d084-112">Area:</span></span>  <br/> |<span data-ttu-id="8d084-113">Common</span><span class="sxs-lookup"><span data-stu-id="8d084-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d084-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d084-114">Remarks</span></span>

<span data-ttu-id="8d084-115">Le type d’objet contenu dans cette propriété correspond à l’interface principale disponible pour un objet accessible par le biais de l’interface **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="8d084-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="8d084-116">Il est généralement obtenue en consultant le paramètre _lpulObjType_ renvoyé par la méthode **OpenEntry** appropriée.</span><span class="sxs-lookup"><span data-stu-id="8d084-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="8d084-117">Lorsque l’interface est obtenue par d’autres moyens, appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8d084-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="8d084-118">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d084-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="8d084-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="8d084-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="8d084-120">Objet conteneur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="8d084-120">Address book container object</span></span> 
    
<span data-ttu-id="8d084-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="8d084-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="8d084-122">Objet Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="8d084-122">Address book object</span></span> 
    
<span data-ttu-id="8d084-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="8d084-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="8d084-124">Objet attachment de message</span><span class="sxs-lookup"><span data-stu-id="8d084-124">Message attachment object</span></span> 
    
<span data-ttu-id="8d084-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8d084-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="8d084-126">Objet liste de distribution</span><span class="sxs-lookup"><span data-stu-id="8d084-126">Distribution list object</span></span> 
    
<span data-ttu-id="8d084-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="8d084-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="8d084-128">Objet Folder</span><span class="sxs-lookup"><span data-stu-id="8d084-128">Folder object</span></span> 
    
<span data-ttu-id="8d084-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="8d084-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="8d084-130">Objet de formulaire</span><span class="sxs-lookup"><span data-stu-id="8d084-130">Form object</span></span> 
    
<span data-ttu-id="8d084-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8d084-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="8d084-132">Messagerie user, objet</span><span class="sxs-lookup"><span data-stu-id="8d084-132">Messaging user object</span></span> 
    
<span data-ttu-id="8d084-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="8d084-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="8d084-134">Message, objet</span><span class="sxs-lookup"><span data-stu-id="8d084-134">Message object</span></span> 
    
<span data-ttu-id="8d084-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="8d084-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="8d084-136">Objet de section de profil</span><span class="sxs-lookup"><span data-stu-id="8d084-136">Profile section object</span></span> 
    
<span data-ttu-id="8d084-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="8d084-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="8d084-138">Objet de la session</span><span class="sxs-lookup"><span data-stu-id="8d084-138">Session object</span></span> 
    
<span data-ttu-id="8d084-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="8d084-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="8d084-140">Objet d’état</span><span class="sxs-lookup"><span data-stu-id="8d084-140">Status object</span></span> 
    
<span data-ttu-id="8d084-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="8d084-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="8d084-142">Objet store de message</span><span class="sxs-lookup"><span data-stu-id="8d084-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8d084-143">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8d084-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d084-144">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8d084-144">Protocol specifications</span></span>

<span data-ttu-id="8d084-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-146">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8d084-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d084-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-147">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-148">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="8d084-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8d084-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-149">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-150">Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().</span><span class="sxs-lookup"><span data-stu-id="8d084-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="8d084-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-151">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-152">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="8d084-152">Handles folder operations.</span></span>
    
<span data-ttu-id="8d084-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-153">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-154">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="8d084-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d084-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-155">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-156">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="8d084-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8d084-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-157">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-158">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="8d084-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8d084-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-159">[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-160">Spécifie les formats de fichiers de carnet en mode hors connexion pour le cache d’objets de livre adresse locale.</span><span class="sxs-lookup"><span data-stu-id="8d084-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="8d084-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-161">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-162">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8d084-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d084-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d084-163">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d084-164">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="8d084-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d084-165">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8d084-165">Header files</span></span>

<span data-ttu-id="8d084-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d084-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d084-167">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8d084-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d084-168">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8d084-168">Mapitags.h</span></span>
  
> <span data-ttu-id="8d084-169">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8d084-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d084-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d084-170">See also</span></span>



[<span data-ttu-id="8d084-171">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8d084-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d084-172">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8d084-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d084-173">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8d084-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d084-174">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8d084-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

