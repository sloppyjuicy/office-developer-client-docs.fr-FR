---
title: Propriété canonique PidLidBirthdayEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4a8cf9ac24f275d8b9cdbe03b5a90477771a2ab4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785077"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="04e97-103">Propriété canonique PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="04e97-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="04e97-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04e97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04e97-105">Spécifie l' **ID d’entrée** d’un rendez-vous facultatif représentant anniversaire du contact.</span><span class="sxs-lookup"><span data-stu-id="04e97-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04e97-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="04e97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04e97-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="04e97-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="04e97-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="04e97-108">Property set:</span></span>  <br/> |<span data-ttu-id="04e97-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="04e97-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="04e97-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="04e97-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04e97-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="04e97-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="04e97-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="04e97-112">Data type:</span></span>  <br/> |<span data-ttu-id="04e97-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="04e97-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="04e97-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="04e97-114">Area:</span></span>  <br/> |<span data-ttu-id="04e97-115">Contact</span><span class="sxs-lookup"><span data-stu-id="04e97-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04e97-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="04e97-116">Remarks</span></span>

<span data-ttu-id="04e97-117">Le rendez-vous que cela est spécifié par cette propriété doit être lié à ce contact à l’aide de la **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) et ** dispidContactLinkName** propriétés ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), comme spécifié dans [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="04e97-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04e97-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="04e97-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04e97-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="04e97-119">Protocol specifications</span></span>

<span data-ttu-id="04e97-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e97-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e97-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="04e97-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04e97-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e97-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e97-123">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="04e97-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04e97-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="04e97-124">Header files</span></span>

<span data-ttu-id="04e97-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04e97-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="04e97-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="04e97-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04e97-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e97-127">See also</span></span>



[<span data-ttu-id="04e97-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="04e97-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04e97-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="04e97-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04e97-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="04e97-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04e97-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="04e97-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

