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
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785662"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="48d37-103">Propriété canonique PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="48d37-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="48d37-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48d37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48d37-105">Contient un masque de bits d’indicateurs indiquant les opérations qui sont disponibles pour le client de l’objet.</span><span class="sxs-lookup"><span data-stu-id="48d37-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48d37-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="48d37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48d37-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="48d37-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="48d37-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="48d37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48d37-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="48d37-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="48d37-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="48d37-110">Data type:</span></span>  <br/> |<span data-ttu-id="48d37-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="48d37-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="48d37-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="48d37-112">Area:</span></span>  <br/> |<span data-ttu-id="48d37-113">Propriétés de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="48d37-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48d37-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="48d37-114">Remarks</span></span>

<span data-ttu-id="48d37-115">Cette propriété est en lecture seule pour le client.</span><span class="sxs-lookup"><span data-stu-id="48d37-115">This property is read-only for the client.</span></span> <span data-ttu-id="48d37-116">Il doit être un binaire **ou** de zéro ou plusieurs valeurs dans le tableau ci-après.</span><span class="sxs-lookup"><span data-stu-id="48d37-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="48d37-117">**Nom**</span><span class="sxs-lookup"><span data-stu-id="48d37-117">**Name**</span></span>|<span data-ttu-id="48d37-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="48d37-118">**Value**</span></span>|<span data-ttu-id="48d37-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="48d37-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48d37-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="48d37-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="48d37-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48d37-121">0x00000001</span></span>  <br/> |<span data-ttu-id="48d37-122">Écriture</span><span class="sxs-lookup"><span data-stu-id="48d37-122">Write</span></span>  <br/> |
|<span data-ttu-id="48d37-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="48d37-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="48d37-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="48d37-124">0x00000002</span></span>  <br/> |<span data-ttu-id="48d37-125">Lire</span><span class="sxs-lookup"><span data-stu-id="48d37-125">Read</span></span>  <br/> |
|<span data-ttu-id="48d37-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="48d37-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="48d37-127">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="48d37-127">0x00000004</span></span>  <br/> |<span data-ttu-id="48d37-128">Suppression</span><span class="sxs-lookup"><span data-stu-id="48d37-128">Delete</span></span>  <br/> |
|<span data-ttu-id="48d37-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="48d37-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="48d37-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="48d37-130">0x00000008</span></span>  <br/> |<span data-ttu-id="48d37-131">Créer des sous-dossiers dans la hiérarchie de dossiers</span><span class="sxs-lookup"><span data-stu-id="48d37-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="48d37-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="48d37-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="48d37-133">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="48d37-133">0x00000010</span></span>  <br/> |<span data-ttu-id="48d37-134">Créer des messages de contenu</span><span class="sxs-lookup"><span data-stu-id="48d37-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="48d37-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="48d37-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="48d37-136">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="48d37-136">0x00000020</span></span>  <br/> |<span data-ttu-id="48d37-137">Créer des messages de contenu associés</span><span class="sxs-lookup"><span data-stu-id="48d37-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="48d37-138">Les indicateurs MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY et MAPI_ACCESS_READ sont trouvent dans le dossier et les objets de message et dans la colonne **PR_ACCESS** dans les tables des matières et contenu associé.</span><span class="sxs-lookup"><span data-stu-id="48d37-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="48d37-139">Les indicateurs MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS et MAPI_ACCESS_CREATE_HIERARCHY sont trouvent sur des objets de dossier uniquement.</span><span class="sxs-lookup"><span data-stu-id="48d37-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48d37-140">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="48d37-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48d37-141">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="48d37-141">Protocol specifications</span></span>

<span data-ttu-id="48d37-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d37-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d37-143">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="48d37-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48d37-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d37-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d37-145">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="48d37-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48d37-146">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="48d37-146">Header files</span></span>

<span data-ttu-id="48d37-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48d37-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="48d37-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="48d37-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="48d37-149">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="48d37-149">Mapitags.h</span></span>
  
> <span data-ttu-id="48d37-150">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="48d37-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48d37-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d37-151">See also</span></span>



[<span data-ttu-id="48d37-152">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="48d37-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48d37-153">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="48d37-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48d37-154">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="48d37-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48d37-155">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="48d37-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

