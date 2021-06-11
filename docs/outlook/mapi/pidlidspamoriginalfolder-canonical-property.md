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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331555"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="507e1-103">Propriété canonique PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="507e1-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="507e1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="507e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="507e1-105">Indique le dossier dans lequel se trouvait un message avant d’être filtré dans le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="507e1-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="507e1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="507e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="507e1-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="507e1-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="507e1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="507e1-108">Property set:</span></span>  <br/> |<span data-ttu-id="507e1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="507e1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="507e1-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="507e1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="507e1-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="507e1-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="507e1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="507e1-112">Data type:</span></span>  <br/> |<span data-ttu-id="507e1-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="507e1-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="507e1-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="507e1-114">Area:</span></span>  <br/> |<span data-ttu-id="507e1-115">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="507e1-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="507e1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="507e1-116">Remarks</span></span>

<span data-ttu-id="507e1-117">La valeur de cette propriété est **l’EntryID** du dossier qui contenait le message avant qu’il ne soit déplacé.</span><span class="sxs-lookup"><span data-stu-id="507e1-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="507e1-118">Cette propriété doit être définie lorsqu’un message est marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="507e1-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="507e1-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="507e1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="507e1-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="507e1-120">Protocol specifications</span></span>

<span data-ttu-id="507e1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="507e1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="507e1-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="507e1-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="507e1-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="507e1-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="507e1-124">Permet la gestion des listes d’adresses de courriers électroniques indésirables et la détermination des listes d’adresses de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="507e1-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="507e1-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="507e1-125">Header files</span></span>

<span data-ttu-id="507e1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="507e1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="507e1-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="507e1-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="507e1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507e1-128">See also</span></span>



[<span data-ttu-id="507e1-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="507e1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="507e1-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="507e1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="507e1-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="507e1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="507e1-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="507e1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

