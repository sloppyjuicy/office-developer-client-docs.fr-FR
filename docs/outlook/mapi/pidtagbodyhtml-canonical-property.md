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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359044"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="f551f-103">Propriété canonique PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="f551f-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="f551f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f551f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f551f-105">Contient la version HTML (Hypertext Markup Language) du texte du message.</span><span class="sxs-lookup"><span data-stu-id="f551f-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f551f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f551f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f551f-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="f551f-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="f551f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f551f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f551f-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="f551f-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="f551f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f551f-110">Data type:</span></span>  <br/> |<span data-ttu-id="f551f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f551f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f551f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f551f-112">Area:</span></span>  <br/> |<span data-ttu-id="f551f-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="f551f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f551f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f551f-114">Remarks</span></span>

<span data-ttu-id="f551f-115">Ces propriétés contiennent le même texte de message que **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mais en HTML.</span><span class="sxs-lookup"><span data-stu-id="f551f-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="f551f-116">Une magasin de messages qui prend en charge le code HTML indique cela en STORE_HTML_OK l’indicateur **PR_STORE_SUPPORT_MASK** **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f551f-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="f551f-117">**Notez** **STORE_HTML_OK** n’est pas défini dans les versions de Mapidefs.h incluses avec Microsoft® Exchange Server 2000 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="f551f-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="f551f-118">Si **STORE_HTML_OK** n’est pas définie, utilisez la valeur 0x00010000 à la place.</span><span class="sxs-lookup"><span data-stu-id="f551f-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f551f-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f551f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f551f-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f551f-120">Protocol specifications</span></span>

<span data-ttu-id="f551f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f551f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f551f-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f551f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f551f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f551f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f551f-124">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f551f-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f551f-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f551f-125">Header files</span></span>

<span data-ttu-id="f551f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f551f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f551f-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f551f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f551f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f551f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f551f-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f551f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f551f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f551f-130">See also</span></span>



[<span data-ttu-id="f551f-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f551f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f551f-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f551f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f551f-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f551f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f551f-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f551f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

