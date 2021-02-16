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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361081"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="fa102-103">Propriété canonique PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="fa102-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="fa102-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa102-105">Contient un identificateur d’objet ASN.1 spécifiant l’application qui a fourni une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fa102-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa102-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fa102-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa102-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="fa102-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="fa102-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fa102-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa102-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="fa102-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="fa102-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fa102-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa102-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fa102-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fa102-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fa102-112">Area:</span></span>  <br/> |<span data-ttu-id="fa102-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="fa102-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa102-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa102-114">Remarks</span></span>

<span data-ttu-id="fa102-115">Cette propriété identifie l’application qui a généré la pièce jointe à l’origine.</span><span class="sxs-lookup"><span data-stu-id="fa102-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="fa102-116">**Remarque** Les **propriétés PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) et **PR_ATTACH_TAG** ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="fa102-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="fa102-117">Elles ne sont ni associées ni associées.</span><span class="sxs-lookup"><span data-stu-id="fa102-117">They are not paired or related.</span></span> <span data-ttu-id="fa102-118">**PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fa102-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="fa102-119">« Object » a une signification beaucoup plus générale dans l’identificateur d’objet de terme et dans l’utilisation X.400 que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="fa102-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="fa102-120">La syntaxe de l’identificateur d’objet et les exemples d’identificateurs d’objet sont définis dans MAPIOID. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="fa102-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="fa102-121">Les **valeurs PR_ATTACH_TAG** ne sont pas limitées à celles définies dans MAPIOID.H.</span><span class="sxs-lookup"><span data-stu-id="fa102-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="fa102-122">Pour plus d’informations sur ces identificateurs d’objets, voir la documentation sur ASN.1, X.208 et X.209.</span><span class="sxs-lookup"><span data-stu-id="fa102-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="fa102-123">L’identificateur d’objet se trouve dans l’élément de référence d’application de l’environnement FTBP (File Transfer Body Part).</span><span class="sxs-lookup"><span data-stu-id="fa102-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fa102-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fa102-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa102-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="fa102-125">Protocol specifications</span></span>

<span data-ttu-id="fa102-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa102-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa102-127">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fa102-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa102-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fa102-128">Header files</span></span>

<span data-ttu-id="fa102-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa102-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa102-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fa102-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa102-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fa102-131">Mapitags.h</span></span>
  
> <span data-ttu-id="fa102-132">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="fa102-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa102-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa102-133">See also</span></span>



[<span data-ttu-id="fa102-134">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="fa102-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="fa102-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fa102-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa102-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fa102-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa102-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fa102-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa102-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fa102-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

