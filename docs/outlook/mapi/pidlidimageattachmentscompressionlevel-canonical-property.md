---
title: Propriété canonique PidLidImageAttachmentsCompressionLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578919"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="169d1-103">Propriété canonique PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="169d1-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="169d1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="169d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="169d1-105">Définit un niveau de compression à appliquer aux pièces jointes de l’image.</span><span class="sxs-lookup"><span data-stu-id="169d1-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="169d1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="169d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="169d1-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="169d1-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="169d1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="169d1-108">Property set:</span></span>  <br/> |<span data-ttu-id="169d1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="169d1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="169d1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="169d1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="169d1-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="169d1-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="169d1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="169d1-112">Data type:</span></span>  <br/> |<span data-ttu-id="169d1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="169d1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="169d1-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="169d1-114">Area:</span></span>  <br/> |<span data-ttu-id="169d1-115">Configuration d’exécution</span><span class="sxs-lookup"><span data-stu-id="169d1-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="169d1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="169d1-116">Remarks</span></span>

<span data-ttu-id="169d1-117">Le niveau de compression sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="169d1-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="169d1-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="169d1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="169d1-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="169d1-119">Protocol specifications</span></span>

<span data-ttu-id="169d1-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="169d1-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="169d1-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="169d1-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="169d1-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="169d1-122">Header files</span></span>

<span data-ttu-id="169d1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="169d1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="169d1-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="169d1-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="169d1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="169d1-125">See also</span></span>



[<span data-ttu-id="169d1-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="169d1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="169d1-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="169d1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="169d1-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="169d1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="169d1-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="169d1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

