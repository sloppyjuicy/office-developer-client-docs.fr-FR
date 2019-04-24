---
title: Propriété canonique PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336322"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="ed9b9-103">Propriété canonique PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="ed9b9-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="ed9b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed9b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed9b9-105">Contient une chaîne Unicode interrogée dans le contenu des pièces jointes de la Banque.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="ed9b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ed9b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed9b9-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="ed9b9-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="ed9b9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ed9b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed9b9-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="ed9b9-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="ed9b9-110">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="ed9b9-110">Property type:</span></span>  <br/> |<span data-ttu-id="ed9b9-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed9b9-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed9b9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ed9b9-112">Area:</span></span>  <br/> |<span data-ttu-id="ed9b9-113">Rechercher</span><span class="sxs-lookup"><span data-stu-id="ed9b9-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ed9b9-114">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="ed9b9-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="ed9b9-115">Cette balise de restriction MAPI, utilisée lors de la recherche de contenu de pièce jointe, ne peut pas être définie dans le fichier d'en-tête téléchargeable dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="ed9b9-116">Vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="ed9b9-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="ed9b9-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ed9b9-117">Protocol specifications</span></span>

<span data-ttu-id="ed9b9-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed9b9-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed9b9-119">Fournit des références aux spécifications de protocole Microsoft Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed9b9-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed9b9-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed9b9-121">Spécifie les propriétés et les opérations pour la manipulation d'une configuration de liste des dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed9b9-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="ed9b9-122">Header files</span></span>

<span data-ttu-id="ed9b9-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ed9b9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed9b9-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed9b9-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ed9b9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ed9b9-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="ed9b9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed9b9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed9b9-127">See also</span></span>



[<span data-ttu-id="ed9b9-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ed9b9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed9b9-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ed9b9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed9b9-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ed9b9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed9b9-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ed9b9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

