---
title: Propriété canonique PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 23d943d5576f5e9d7694b03c90dea79a878dee64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785757"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="f008c-103">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="f008c-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="f008c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f008c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f008c-105">Contient le texte du message.</span><span class="sxs-lookup"><span data-stu-id="f008c-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f008c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f008c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f008c-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="f008c-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="f008c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f008c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f008c-109">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="f008c-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="f008c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f008c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f008c-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f008c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f008c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="f008c-112">Area:</span></span>  <br/> |<span data-ttu-id="f008c-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="f008c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f008c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f008c-114">Remarks</span></span>

<span data-ttu-id="f008c-115">Ces propriétés sont généralement utilisées uniquement dans un message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="f008c-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="f008c-116">Banques de messages qui prennent en charge le Format RTF (RICH Text Format) ignorent toutes les modifications dans l’espace blanc dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="f008c-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="f008c-117">Lorsque **PR_BODY** est stockée pour la première fois, la banque de messages également génère et stocke la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message.</span><span class="sxs-lookup"><span data-stu-id="f008c-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="f008c-118">Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifié, la banque de messages appelle la fonction de [RTFSync](rtfsync.md) pour assurer la synchronisation avec la version RTF.</span><span class="sxs-lookup"><span data-stu-id="f008c-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="f008c-119">Si seule l’espace blanc a été modifié, les propriétés restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="f008c-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="f008c-120">Ainsi, n’importe quel format RTF important mise en forme lorsque le message transite par non RTF-prenant en charge les clients et les systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f008c-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="f008c-121">La valeur de cette propriété doit être exprimée dans la page de codes du système d’exploitation exécuté sur MAPI.</span><span class="sxs-lookup"><span data-stu-id="f008c-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f008c-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f008c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f008c-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f008c-123">Protocol specifications</span></span>

<span data-ttu-id="f008c-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f008c-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f008c-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f008c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f008c-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f008c-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f008c-127">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f008c-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f008c-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f008c-128">Header files</span></span>

<span data-ttu-id="f008c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f008c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f008c-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f008c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="f008c-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f008c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="f008c-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f008c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f008c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f008c-133">See also</span></span>



[<span data-ttu-id="f008c-134">Propriété canonique PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="f008c-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="f008c-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f008c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f008c-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f008c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f008c-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f008c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f008c-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f008c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

