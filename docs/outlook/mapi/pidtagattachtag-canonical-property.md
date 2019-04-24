---
title: Propriété canonique PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361081"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="9d201-103">Propriété canonique PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="9d201-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="9d201-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d201-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d201-105">Contient un identificateur d'objet ASN. 1 spécifiant l'application qui a fourni une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9d201-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d201-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d201-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d201-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="9d201-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="9d201-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d201-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d201-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="9d201-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="9d201-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d201-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d201-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d201-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d201-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9d201-112">Area:</span></span>  <br/> |<span data-ttu-id="9d201-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="9d201-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d201-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d201-114">Remarks</span></span>

<span data-ttu-id="9d201-115">Cette propriété identifie l'application qui a initialement généré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9d201-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="9d201-116">**Note** Les propriétés **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) et **PR_ATTACH_TAG** ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="9d201-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="9d201-117">Elles ne sont pas couplées ni associées.</span><span class="sxs-lookup"><span data-stu-id="9d201-117">They are not paired or related.</span></span> <span data-ttu-id="9d201-118">**PR_ATTACH_ENCODING** identifie l'algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9d201-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="9d201-119">«Object» a une signification bien plus générale dans le terme identificateur d'objet, et dans l'utilisation de X. 400, que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="9d201-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="9d201-120">La syntaxe de l'identificateur d'objet et des exemples d'identificateurs d'objet sont définis dans le MAPIOID. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="9d201-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="9d201-121">Les valeurs de **PR_ATTACH_TAG** ne sont pas limitées à celles définies dans MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="9d201-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="9d201-122">Pour plus d'informations sur ces identificateurs d'objet, reportez-vous à la documentation sur ASN. 1, X. 208 et X. 209.</span><span class="sxs-lookup"><span data-stu-id="9d201-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="9d201-123">L'identificateur de l'objet est disponible dans l'élément de référence de l'application de l'environnement du corps du transfert de fichiers (FTBP).</span><span class="sxs-lookup"><span data-stu-id="9d201-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d201-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9d201-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d201-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9d201-125">Protocol specifications</span></span>

<span data-ttu-id="9d201-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d201-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d201-127">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="9d201-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d201-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9d201-128">Header files</span></span>

<span data-ttu-id="9d201-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9d201-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d201-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d201-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d201-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9d201-131">Mapitags.h</span></span>
  
> <span data-ttu-id="9d201-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9d201-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d201-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d201-133">See also</span></span>



[<span data-ttu-id="9d201-134">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="9d201-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="9d201-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d201-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d201-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d201-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d201-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d201-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d201-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9d201-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

