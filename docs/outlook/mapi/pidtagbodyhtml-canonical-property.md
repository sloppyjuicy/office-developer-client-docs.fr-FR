---
title: Propriété canonique PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785767"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="6b403-103">Propriété canonique PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="6b403-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="6b403-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b403-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b403-105">Contient la version de langage HTML (Hypertext Markup) du texte du message.</span><span class="sxs-lookup"><span data-stu-id="6b403-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b403-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6b403-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b403-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="6b403-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="6b403-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6b403-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b403-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="6b403-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="6b403-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6b403-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b403-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6b403-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6b403-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6b403-112">Area:</span></span>  <br/> |<span data-ttu-id="6b403-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="6b403-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b403-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b403-114">Remarks</span></span>

<span data-ttu-id="6b403-115">Ces propriétés contiennent le texte du message même en tant que la **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mais dans le code HTML.</span><span class="sxs-lookup"><span data-stu-id="6b403-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="6b403-116">Une banque de messages qui prend en charge HTML indique qu’il en définissant l’indicateur **STORE_HTML_OK** dans son **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6b403-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="6b403-117">**Remarque** **STORE_HTML_OK** n’est pas défini dans les versions de Mapidefs.h inclus avec Microsoft® Exchange Server 2000 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="6b403-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="6b403-118">Si **STORE_HTML_OK** n’est pas défini, utilisez plutôt la valeur 0 x 00010000.</span><span class="sxs-lookup"><span data-stu-id="6b403-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6b403-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6b403-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b403-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6b403-120">Protocol specifications</span></span>

<span data-ttu-id="6b403-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b403-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b403-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6b403-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b403-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b403-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b403-124">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6b403-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b403-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6b403-125">Header files</span></span>

<span data-ttu-id="6b403-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b403-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b403-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6b403-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b403-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6b403-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6b403-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6b403-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b403-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b403-130">See also</span></span>



[<span data-ttu-id="6b403-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6b403-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b403-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6b403-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b403-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6b403-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b403-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6b403-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

