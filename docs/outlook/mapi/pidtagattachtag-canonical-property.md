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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400452"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="efeaa-103">Propriété canonique PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="efeaa-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="efeaa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efeaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efeaa-105">Contient un identificateur d’objet ASN.1 spécifiant l’application d'où provient d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="efeaa-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="efeaa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="efeaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efeaa-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="efeaa-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="efeaa-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="efeaa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efeaa-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="efeaa-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="efeaa-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="efeaa-110">Data type:</span></span>  <br/> |<span data-ttu-id="efeaa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="efeaa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="efeaa-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="efeaa-112">Area:</span></span>  <br/> |<span data-ttu-id="efeaa-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="efeaa-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efeaa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="efeaa-114">Remarks</span></span>

<span data-ttu-id="efeaa-115">Cette propriété identifie l’application qui a généré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="efeaa-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="efeaa-116">**Remarque** Les propriétés **PR_ATTACH_TAG** et **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="efeaa-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="efeaa-117">Ils ne sont pas couplés ou liées.</span><span class="sxs-lookup"><span data-stu-id="efeaa-117">They are not paired or related.</span></span> <span data-ttu-id="efeaa-118">**PR_ATTACH_ENCODING** identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="efeaa-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="efeaa-119">« Objet » a une signification plus générale dans l’identificateur d’objet termes et l’utilisation X.400, que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="efeaa-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="efeaa-120">Les identificateurs d’objets objet identificateur la syntaxe et les exemples sont définies dans le MAPIOID. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="efeaa-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="efeaa-121">Valeurs de **PR_ATTACH_TAG** ne sont pas limités à ceux définis dans MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="efeaa-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="efeaa-122">Pour plus d’informations sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209.</span><span class="sxs-lookup"><span data-stu-id="efeaa-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="efeaa-123">L’identificateur d’objet est trouvé dans l’élément de référence de l’application de l’environnement de fichier transférer corps composant FTBP ().</span><span class="sxs-lookup"><span data-stu-id="efeaa-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="efeaa-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="efeaa-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efeaa-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="efeaa-125">Protocol specifications</span></span>

<span data-ttu-id="efeaa-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efeaa-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efeaa-127">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="efeaa-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efeaa-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="efeaa-128">Header files</span></span>

<span data-ttu-id="efeaa-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efeaa-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="efeaa-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="efeaa-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="efeaa-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="efeaa-131">Mapitags.h</span></span>
  
> <span data-ttu-id="efeaa-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="efeaa-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efeaa-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efeaa-133">See also</span></span>



[<span data-ttu-id="efeaa-134">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="efeaa-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="efeaa-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="efeaa-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efeaa-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="efeaa-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efeaa-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="efeaa-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efeaa-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="efeaa-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

