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
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="9f467-103">Propriété canonique PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="9f467-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="9f467-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f467-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f467-105">Contient la version HTML (Hypertext Markup Language) du texte du message.</span><span class="sxs-lookup"><span data-stu-id="9f467-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f467-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9f467-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f467-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="9f467-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="9f467-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9f467-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f467-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="9f467-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="9f467-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9f467-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f467-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9f467-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9f467-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9f467-112">Area:</span></span>  <br/> |<span data-ttu-id="9f467-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="9f467-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f467-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f467-114">Remarks</span></span>

<span data-ttu-id="9f467-115">Ces propriétés contiennent le même texte de message que **le PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mais en HTML.</span><span class="sxs-lookup"><span data-stu-id="9f467-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="9f467-116">Une magasin de messages qui prend en charge le code HTML indique cela en STORE_HTML_OK l’indicateur **PR_STORE_SUPPORT_MASK** **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9f467-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="9f467-117">**Notez** **STORE_HTML_OK** n’est pas défini dans les versions de Mapidefs.h incluses avec Microsoft® Exchange 2000 Server et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="9f467-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="9f467-118">Si **STORE_HTML_OK** n’est pas définie, utilisez la valeur 0x00010000 à la place.</span><span class="sxs-lookup"><span data-stu-id="9f467-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9f467-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9f467-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f467-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9f467-120">Protocol specifications</span></span>

<span data-ttu-id="9f467-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f467-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f467-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="9f467-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f467-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f467-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f467-124">Gère les objets de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9f467-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f467-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9f467-125">Header files</span></span>

<span data-ttu-id="9f467-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f467-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f467-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9f467-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f467-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f467-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9f467-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9f467-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f467-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f467-130">See also</span></span>



[<span data-ttu-id="9f467-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9f467-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f467-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9f467-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f467-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9f467-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f467-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9f467-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

