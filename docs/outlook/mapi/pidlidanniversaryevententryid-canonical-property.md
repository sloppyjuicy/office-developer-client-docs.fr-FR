---
title: Propriété canonique PidLidAnniversaryEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b20234d079fb38fac878efe92390defcba6e5d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335573"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="e0ebb-103">Propriété canonique PidLidAnniversaryEventEntryId</span><span class="sxs-lookup"><span data-stu-id="e0ebb-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e0ebb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0ebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0ebb-105">Spécifie l’identificateur d’entrée du rendez-vous qui représente l’anniversaire du contact.</span><span class="sxs-lookup"><span data-stu-id="e0ebb-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0ebb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e0ebb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0ebb-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="e0ebb-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="e0ebb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e0ebb-108">Property set:</span></span>  <br/> |<span data-ttu-id="e0ebb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e0ebb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e0ebb-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="e0ebb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e0ebb-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="e0ebb-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="e0ebb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e0ebb-112">Data type:</span></span>  <br/> |<span data-ttu-id="e0ebb-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e0ebb-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e0ebb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e0ebb-114">Area:</span></span>  <br/> |<span data-ttu-id="e0ebb-115">Contact</span><span class="sxs-lookup"><span data-stu-id="e0ebb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0ebb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0ebb-116">Remarks</span></span>

<span data-ttu-id="e0ebb-117">Le rendez-vous spécifié par la propriété **dispidAnniversaryEventEID** doit être lié à ce contact à l’aide des propriétés **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) et **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), comme détaillé dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0ebb-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0ebb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e0ebb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0ebb-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e0ebb-119">Protocol specifications</span></span>

<span data-ttu-id="e0ebb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0ebb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0ebb-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="e0ebb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0ebb-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0ebb-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0ebb-123">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="e0ebb-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0ebb-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e0ebb-124">Header files</span></span>

<span data-ttu-id="e0ebb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0ebb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0ebb-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e0ebb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0ebb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0ebb-127">See also</span></span>



[<span data-ttu-id="e0ebb-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e0ebb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0ebb-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e0ebb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0ebb-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e0ebb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0ebb-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e0ebb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

