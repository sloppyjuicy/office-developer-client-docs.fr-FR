---
title: Propriété canonique PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316512"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="459e3-103">Propriété canonique PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="459e3-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="459e3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="459e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="459e3-105">Contient un masque de masque des indicateurs indiquant les opérations qui sont disponibles pour le client pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="459e3-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="459e3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="459e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="459e3-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="459e3-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="459e3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="459e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="459e3-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="459e3-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="459e3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="459e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="459e3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="459e3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="459e3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="459e3-112">Area:</span></span>  <br/> |<span data-ttu-id="459e3-113">Propriétés de contrôle d'accès</span><span class="sxs-lookup"><span data-stu-id="459e3-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="459e3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="459e3-114">Remarks</span></span>

<span data-ttu-id="459e3-115">Cette propriété est en lecture seule pour le client.</span><span class="sxs-lookup"><span data-stu-id="459e3-115">This property is read-only for the client.</span></span> <span data-ttu-id="459e3-116">Il doit s'agir d' \*\*\*\* une opération de bits or de zéro ou plusieurs valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="459e3-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="459e3-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="459e3-117">**Name**</span></span>|<span data-ttu-id="459e3-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="459e3-118">**Value**</span></span>|<span data-ttu-id="459e3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="459e3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="459e3-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="459e3-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="459e3-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="459e3-121">0x00000001</span></span>  <br/> |<span data-ttu-id="459e3-122">Écrire</span><span class="sxs-lookup"><span data-stu-id="459e3-122">Write</span></span>  <br/> |
|<span data-ttu-id="459e3-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="459e3-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="459e3-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="459e3-124">0x00000002</span></span>  <br/> |<span data-ttu-id="459e3-125">Lecture</span><span class="sxs-lookup"><span data-stu-id="459e3-125">Read</span></span>  <br/> |
|<span data-ttu-id="459e3-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="459e3-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="459e3-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="459e3-127">0x00000004</span></span>  <br/> |<span data-ttu-id="459e3-128">Supprimer</span><span class="sxs-lookup"><span data-stu-id="459e3-128">Delete</span></span>  <br/> |
|<span data-ttu-id="459e3-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="459e3-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="459e3-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="459e3-130">0x00000008</span></span>  <br/> |<span data-ttu-id="459e3-131">Créer des sous-dossiers dans la hiérarchie de dossiers</span><span class="sxs-lookup"><span data-stu-id="459e3-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="459e3-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="459e3-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="459e3-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="459e3-133">0x00000010</span></span>  <br/> |<span data-ttu-id="459e3-134">Créer des messages de contenu</span><span class="sxs-lookup"><span data-stu-id="459e3-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="459e3-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="459e3-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="459e3-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="459e3-136">0x00000020</span></span>  <br/> |<span data-ttu-id="459e3-137">Créer des messages de contenu associés</span><span class="sxs-lookup"><span data-stu-id="459e3-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="459e3-138">Les indicateurs MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY et MAPI_ACCESS_READ sont disponibles sur les objets Folder et message, ainsi que dans la colonne **PR_ACCESS** des tables des matières et des tables des matières associées.</span><span class="sxs-lookup"><span data-stu-id="459e3-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="459e3-139">Les indicateurs MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS et MAPI_ACCESS_CREATE_HIERARCHY se trouvent uniquement sur les objets Folder.</span><span class="sxs-lookup"><span data-stu-id="459e3-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="459e3-140">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="459e3-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="459e3-141">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="459e3-141">Protocol specifications</span></span>

<span data-ttu-id="459e3-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="459e3-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="459e3-143">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="459e3-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="459e3-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="459e3-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="459e3-145">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="459e3-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="459e3-146">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="459e3-146">Header files</span></span>

<span data-ttu-id="459e3-147">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="459e3-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="459e3-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="459e3-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="459e3-149">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="459e3-149">Mapitags.h</span></span>
  
> <span data-ttu-id="459e3-150">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="459e3-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="459e3-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="459e3-151">See also</span></span>



[<span data-ttu-id="459e3-152">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="459e3-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="459e3-153">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="459e3-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="459e3-154">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="459e3-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="459e3-155">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="459e3-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

