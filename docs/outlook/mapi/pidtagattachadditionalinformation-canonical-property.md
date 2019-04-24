---
title: Propriété canonique PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339871"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="3c1df-103">Propriété canonique PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="3c1df-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="3c1df-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c1df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c1df-105">Fournit des informations sur le type de fichier pour une pièce jointe non Windows.</span><span class="sxs-lookup"><span data-stu-id="3c1df-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c1df-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3c1df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c1df-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="3c1df-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="3c1df-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3c1df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c1df-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="3c1df-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="3c1df-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3c1df-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c1df-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c1df-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c1df-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3c1df-112">Area:</span></span>  <br/> |<span data-ttu-id="3c1df-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="3c1df-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c1df-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c1df-114">Remarks</span></span>

<span data-ttu-id="3c1df-115">Cette propriété fournit des métadonnées relatives à une pièce jointe spécifique en fonction de l'encodage de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c1df-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="3c1df-116">Par exemple, lorsque la propriété **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contient MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contient une chaîne qui représente le créateur de fichier Macintosh et le type de fichier, mis en forme comme suit: «: Crea: type» pour le fichier Macintosh encodé.</span><span class="sxs-lookup"><span data-stu-id="3c1df-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c1df-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="3c1df-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c1df-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3c1df-118">Protocol specifications</span></span>

<span data-ttu-id="3c1df-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c1df-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c1df-120">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="3c1df-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c1df-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3c1df-121">Header files</span></span>

<span data-ttu-id="3c1df-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3c1df-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c1df-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3c1df-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c1df-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3c1df-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3c1df-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="3c1df-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c1df-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c1df-126">See also</span></span>



[<span data-ttu-id="3c1df-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1df-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c1df-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1df-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c1df-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3c1df-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c1df-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3c1df-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

