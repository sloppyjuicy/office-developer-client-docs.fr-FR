---
title: Propriété canonique PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4cb0243f38137afa820c3499a8b95954098bd6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785435"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="fbbed-103">Propriété canonique PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="fbbed-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="fbbed-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbbed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbbed-105">Indique quel dossier un message se trouvait avant qu’il a été filtré dans le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fbbed-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbbed-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fbbed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbbed-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="fbbed-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="fbbed-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="fbbed-108">Property set:</span></span>  <br/> |<span data-ttu-id="fbbed-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fbbed-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fbbed-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="fbbed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fbbed-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="fbbed-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="fbbed-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fbbed-112">Data type:</span></span>  <br/> |<span data-ttu-id="fbbed-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fbbed-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fbbed-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="fbbed-114">Area:</span></span>  <br/> |<span data-ttu-id="fbbed-115">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="fbbed-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbbed-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fbbed-116">Remarks</span></span>

<span data-ttu-id="fbbed-117">La valeur de cette propriété est **propriété EntryID** du dossier qui contenue le message avant d’être déplacée.</span><span class="sxs-lookup"><span data-stu-id="fbbed-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="fbbed-118">Cette propriété doit être définie lorsqu’un message est marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fbbed-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fbbed-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fbbed-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fbbed-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="fbbed-120">Protocol specifications</span></span>

<span data-ttu-id="fbbed-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbbed-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbbed-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="fbbed-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fbbed-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbbed-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbbed-124">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="fbbed-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fbbed-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fbbed-125">Header files</span></span>

<span data-ttu-id="fbbed-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbbed-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbbed-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fbbed-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbbed-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbbed-128">See also</span></span>



[<span data-ttu-id="fbbed-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fbbed-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fbbed-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fbbed-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbbed-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fbbed-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbbed-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="fbbed-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

