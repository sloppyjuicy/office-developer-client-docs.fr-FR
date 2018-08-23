---
title: Propriété canonique PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 80d1fc3f711369471eb2c1473700f13a6b995594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578506"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="9e772-103">Propriété canonique PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="9e772-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="9e772-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e772-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e772-105">Contient une chaîne Unicode qui est interrogée dans le contenu de pièce jointe dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="9e772-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="9e772-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9e772-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e772-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="9e772-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="9e772-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9e772-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e772-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="9e772-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="9e772-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="9e772-110">Property type:</span></span>  <br/> |<span data-ttu-id="9e772-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e772-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9e772-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9e772-112">Area:</span></span>  <br/> |<span data-ttu-id="9e772-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="9e772-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9e772-114">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9e772-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="9e772-115">Cette balise de restriction MAPI, utilisée lorsque vous effectuez une recherche de contenu de pièce jointe, pas peut-être être définie dans le fichier d’en-tête téléchargeable dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="9e772-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="9e772-116">Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="9e772-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="9e772-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9e772-117">Protocol specifications</span></span>

<span data-ttu-id="9e772-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e772-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e772-119">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9e772-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e772-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e772-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e772-121">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="9e772-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e772-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9e772-122">Header files</span></span>

<span data-ttu-id="9e772-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e772-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e772-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9e772-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e772-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9e772-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9e772-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9e772-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e772-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e772-127">See also</span></span>



[<span data-ttu-id="9e772-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9e772-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e772-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9e772-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e772-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9e772-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e772-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9e772-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

