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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413828"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="3c330-103">Propriété canonique PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="3c330-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="3c330-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c330-105">Définit un niveau de compression à appliquer aux pièces jointes d’image.</span><span class="sxs-lookup"><span data-stu-id="3c330-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c330-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3c330-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c330-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="3c330-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="3c330-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3c330-108">Property set:</span></span>  <br/> |<span data-ttu-id="3c330-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3c330-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3c330-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="3c330-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3c330-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="3c330-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="3c330-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3c330-112">Data type:</span></span>  <br/> |<span data-ttu-id="3c330-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c330-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c330-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3c330-114">Area:</span></span>  <br/> |<span data-ttu-id="3c330-115">Configuration au moment de l’exécuter</span><span class="sxs-lookup"><span data-stu-id="3c330-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c330-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c330-116">Remarks</span></span>

<span data-ttu-id="3c330-117">Les niveaux de compression valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3c330-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="3c330-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3c330-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c330-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3c330-119">Protocol specifications</span></span>

<span data-ttu-id="3c330-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3c330-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3c330-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="3c330-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c330-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3c330-122">Header files</span></span>

<span data-ttu-id="3c330-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c330-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c330-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3c330-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c330-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c330-125">See also</span></span>



[<span data-ttu-id="3c330-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3c330-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c330-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3c330-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c330-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3c330-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c330-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3c330-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

