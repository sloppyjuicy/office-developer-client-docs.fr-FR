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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326634"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="8a17a-103">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="8a17a-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="8a17a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a17a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a17a-105">Contient le texte du message.</span><span class="sxs-lookup"><span data-stu-id="8a17a-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a17a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8a17a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a17a-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="8a17a-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="8a17a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8a17a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a17a-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="8a17a-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="8a17a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8a17a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a17a-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8a17a-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8a17a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8a17a-112">Area:</span></span>  <br/> |<span data-ttu-id="8a17a-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="8a17a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a17a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a17a-114">Remarks</span></span>

<span data-ttu-id="8a17a-115">Ces propriétés sont généralement utilisées uniquement dans un message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="8a17a-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="8a17a-116">Les magasins de messages qui prendre en charge le format RTF (Rich Text Format) ignorent les modifications apportées aux espaces dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="8a17a-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="8a17a-117">Lorsque **PR_BODY** est stocké pour la première fois, la boutique de messages génère et stocke également la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message.</span><span class="sxs-lookup"><span data-stu-id="8a17a-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="8a17a-118">Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée et **que PR_BODY a** été modifié, la boutique de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF.</span><span class="sxs-lookup"><span data-stu-id="8a17a-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="8a17a-119">Si seuls des espaces ont été modifiés, les propriétés restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="8a17a-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="8a17a-120">Cela permet de conserver toute mise en forme RTF nontrivial lorsque le message passe par des clients et des systèmes de messagerie non RTF.</span><span class="sxs-lookup"><span data-stu-id="8a17a-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="8a17a-121">La valeur de cette propriété doit être exprimée dans la page de code du système d’exploitation sur qui MAPI s’exécute.</span><span class="sxs-lookup"><span data-stu-id="8a17a-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8a17a-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8a17a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a17a-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8a17a-123">Protocol specifications</span></span>

<span data-ttu-id="8a17a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a17a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a17a-125">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8a17a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a17a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a17a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a17a-127">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="8a17a-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a17a-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8a17a-128">Header files</span></span>

<span data-ttu-id="8a17a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a17a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a17a-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8a17a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a17a-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a17a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="8a17a-132">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="8a17a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a17a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a17a-133">See also</span></span>



[<span data-ttu-id="8a17a-134">Propriété canonique PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="8a17a-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="8a17a-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8a17a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a17a-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8a17a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a17a-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8a17a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a17a-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8a17a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

