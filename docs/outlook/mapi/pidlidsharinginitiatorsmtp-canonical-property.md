---
title: Propriété canonique PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391450"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="4d71d-103">Propriété canonique PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="4d71d-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="4d71d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d71d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d71d-105">Spécifie l’adresse SMTP de l’utilisateur qui a initié le message de partage.</span><span class="sxs-lookup"><span data-stu-id="4d71d-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="4d71d-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="4d71d-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d71d-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4d71d-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d71d-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="4d71d-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="4d71d-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="4d71d-109">Property set:</span></span>  <br/> |<span data-ttu-id="4d71d-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="4d71d-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="4d71d-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="4d71d-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4d71d-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="4d71d-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="4d71d-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4d71d-113">Data type:</span></span>  <br/> |<span data-ttu-id="4d71d-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d71d-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d71d-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4d71d-115">Area:</span></span>  <br/> |<span data-ttu-id="4d71d-116">Partage</span><span class="sxs-lookup"><span data-stu-id="4d71d-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d71d-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d71d-117">Remarks</span></span>

<span data-ttu-id="4d71d-118">Cette propriété doit être définie sur la valeur de la propriété **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) à partir du carnet d’adresses identifiée par la propriété **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) et doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="4d71d-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d71d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4d71d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d71d-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4d71d-120">Protocol specifications</span></span>

<span data-ttu-id="4d71d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d71d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d71d-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="4d71d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d71d-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d71d-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d71d-124">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="4d71d-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d71d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4d71d-125">Header files</span></span>

<span data-ttu-id="4d71d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d71d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d71d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4d71d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d71d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d71d-128">See also</span></span>



[<span data-ttu-id="4d71d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4d71d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d71d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4d71d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d71d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4d71d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d71d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4d71d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

