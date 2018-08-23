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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: af5d05ee6d3592694952002c16e16188c3e458a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565619"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="38cbb-103">Propriété canonique PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="38cbb-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="38cbb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38cbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38cbb-105">Contient un identificateur d’objet ASN.1 spécifiant l’application d'où provient d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38cbb-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38cbb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="38cbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38cbb-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="38cbb-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="38cbb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="38cbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38cbb-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="38cbb-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="38cbb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="38cbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="38cbb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="38cbb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="38cbb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="38cbb-112">Area:</span></span>  <br/> |<span data-ttu-id="38cbb-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="38cbb-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38cbb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="38cbb-114">Remarks</span></span>

<span data-ttu-id="38cbb-115">Cette propriété identifie l’application qui a généré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38cbb-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="38cbb-116">**Remarque** Les propriétés **PR_ATTACH_TAG** et **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="38cbb-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="38cbb-117">Ils ne sont pas couplés ou liées.</span><span class="sxs-lookup"><span data-stu-id="38cbb-117">They are not paired or related.</span></span> <span data-ttu-id="38cbb-118">**PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38cbb-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="38cbb-119">« Objet » a une signification plus générale dans l’identificateur d’objet termes et l’utilisation X.400, que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="38cbb-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="38cbb-120">Les identificateurs d’objets objet identificateur la syntaxe et les exemples sont définies dans le MAPIOID. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="38cbb-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="38cbb-121">Valeurs de **PR_ATTACH_TAG** ne sont pas limités à ceux définis dans MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="38cbb-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="38cbb-122">Pour plus d’informations sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209.</span><span class="sxs-lookup"><span data-stu-id="38cbb-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="38cbb-123">L’identificateur d’objet est trouvé dans l’élément de référence de l’application de l’environnement de fichier transférer corps composant FTBP ().</span><span class="sxs-lookup"><span data-stu-id="38cbb-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="38cbb-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="38cbb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38cbb-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="38cbb-125">Protocol specifications</span></span>

<span data-ttu-id="38cbb-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38cbb-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38cbb-127">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38cbb-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38cbb-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="38cbb-128">Header files</span></span>

<span data-ttu-id="38cbb-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38cbb-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="38cbb-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="38cbb-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="38cbb-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="38cbb-131">Mapitags.h</span></span>
  
> <span data-ttu-id="38cbb-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="38cbb-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38cbb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38cbb-133">See also</span></span>



[<span data-ttu-id="38cbb-134">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="38cbb-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="38cbb-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="38cbb-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38cbb-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="38cbb-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38cbb-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="38cbb-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38cbb-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="38cbb-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

