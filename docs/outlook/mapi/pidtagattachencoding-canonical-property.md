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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7475eef15398081a30307e7b4a077a0700a6ba8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584197"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="ee594-103">Propriété canonique PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="ee594-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="ee594-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee594-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee594-105">Contient un identificateur d’objet ASN.1 qui spécifie le codage d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ee594-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee594-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ee594-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee594-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="ee594-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="ee594-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ee594-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee594-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="ee594-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="ee594-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ee594-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee594-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ee594-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ee594-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ee594-112">Area:</span></span>  <br/> |<span data-ttu-id="ee594-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="ee594-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee594-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee594-114">Remarks</span></span>

<span data-ttu-id="ee594-115">Cette propriété identifie l’algorithme utilisé pour transformer les données dans une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ee594-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="ee594-116">**Remarque** Les **PR_ATTACH_ENCODING** et les propriétés de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="ee594-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="ee594-117">Ils ne sont pas couplés ou liées.</span><span class="sxs-lookup"><span data-stu-id="ee594-117">They are not paired or related.</span></span> <span data-ttu-id="ee594-118">**PR_ATTACH_TAG** identifie l’application qui a généré la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ee594-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="ee594-119">« Objet » a une signification beaucoup plus générale X.400 et l’identificateur d’objet termes que dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="ee594-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="ee594-120">Les identificateurs d’objets objet identificateur la syntaxe et les exemples sont définies dans le MAPIOID. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="ee594-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="ee594-121">Valeurs de **PR_ATTACH_ENCODING** ne sont pas limités à ceux définis dans MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="ee594-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="ee594-122">Par exemple, les fichiers Macintosh joints permet un identificateur tel que MacBinary.</span><span class="sxs-lookup"><span data-stu-id="ee594-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="ee594-123">Pour plus d’informations sur ces identificateurs d’objet, consultez la documentation sur ASN.1, X.208 et X.209.</span><span class="sxs-lookup"><span data-stu-id="ee594-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="ee594-124">L’identificateur d’objet est trouvé dans l’élément de référence de l’application de l’environnement FTBP (File Transfer Body Part).</span><span class="sxs-lookup"><span data-stu-id="ee594-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee594-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ee594-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee594-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ee594-126">Protocol specifications</span></span>

<span data-ttu-id="ee594-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee594-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee594-128">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ee594-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee594-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ee594-129">Header files</span></span>

<span data-ttu-id="ee594-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee594-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee594-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ee594-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee594-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ee594-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ee594-133">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ee594-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee594-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee594-134">See also</span></span>



[<span data-ttu-id="ee594-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ee594-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee594-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ee594-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee594-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ee594-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee594-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ee594-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

