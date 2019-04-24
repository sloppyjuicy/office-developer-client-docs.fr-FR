---
title: Propriété canonique PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345492"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="6e97e-103">Propriété canonique PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="6e97e-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="6e97e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e97e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e97e-105">Contient un identificateur d'objet ASN. 1 qui spécifie le codage d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6e97e-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e97e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e97e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e97e-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="6e97e-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="6e97e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6e97e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e97e-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="6e97e-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="6e97e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e97e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e97e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e97e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e97e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6e97e-112">Area:</span></span>  <br/> |<span data-ttu-id="6e97e-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="6e97e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e97e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e97e-114">Remarks</span></span>

<span data-ttu-id="6e97e-115">Cette propriété identifie l'algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6e97e-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="6e97e-116">**Note** Les propriétés **PR_ATTACH_ENCODING** et **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="6e97e-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="6e97e-117">Elles ne sont pas couplées ni associées.</span><span class="sxs-lookup"><span data-stu-id="6e97e-117">They are not paired or related.</span></span> <span data-ttu-id="6e97e-118">**PR_ATTACH_TAG** identifie l'application qui a initialement généré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6e97e-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="6e97e-119">«Object» a une signification bien plus générale dans le terme identificateur d'objet et dans X. 400, que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="6e97e-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="6e97e-120">La syntaxe de l'identificateur d'objet et des exemples d'identificateurs d'objet sont définis dans le MAPIOID. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="6e97e-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="6e97e-121">Les valeurs de **PR_ATTACH_ENCODING** ne sont pas limitées à celles définies dans MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="6e97e-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="6e97e-122">Par exemple, les fichiers Macintosh attachés peuvent utiliser un identificateur tel que MacBinary.</span><span class="sxs-lookup"><span data-stu-id="6e97e-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="6e97e-123">Pour plus d'informations sur ces identificateurs d'objet, reportez-vous à la documentation sur ASN. 1, X. 208 et X. 209.</span><span class="sxs-lookup"><span data-stu-id="6e97e-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="6e97e-124">L'identificateur de l'objet est disponible dans l'élément de référence de l'application de l'environnement FTBP (partie du corps du transfert de fichiers).</span><span class="sxs-lookup"><span data-stu-id="6e97e-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e97e-125">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="6e97e-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e97e-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6e97e-126">Protocol specifications</span></span>

<span data-ttu-id="6e97e-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e97e-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e97e-128">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="6e97e-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e97e-129">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="6e97e-129">Header files</span></span>

<span data-ttu-id="6e97e-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6e97e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e97e-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e97e-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e97e-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6e97e-132">Mapitags.h</span></span>
  
> <span data-ttu-id="6e97e-133">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="6e97e-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e97e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e97e-134">See also</span></span>



[<span data-ttu-id="6e97e-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e97e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e97e-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e97e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e97e-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e97e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e97e-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6e97e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

