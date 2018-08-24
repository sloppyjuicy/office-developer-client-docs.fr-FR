---
title: Propriété canonique PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dc31d26ba1aa695ad0b64114ac7992e10bb548ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595407"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="27b84-103">Propriété canonique PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="27b84-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="27b84-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27b84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27b84-105">Indique si les destinataires de messagerie à ajouter à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="27b84-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27b84-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27b84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27b84-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="27b84-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="27b84-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="27b84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27b84-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="27b84-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="27b84-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27b84-110">Data type:</span></span>  <br/> |<span data-ttu-id="27b84-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27b84-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27b84-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="27b84-112">Area:</span></span>  <br/> |<span data-ttu-id="27b84-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="27b84-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27b84-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="27b84-114">Remarks</span></span>

<span data-ttu-id="27b84-115">Le cas échéant, cette propriété doit être définie sur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="27b84-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="27b84-116">Une valeur de 1 indique que les destinataires de messagerie sont à ajouter à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="27b84-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="27b84-117">Une valeur de 0 indique que les destinataires de messagerie ne doivent ne pas figurer dans la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="27b84-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="27b84-118">Si cette propriété est présente avec la valeur 1, les adresses SMTP des destinataires de courrier électronique doivent être ajoutés à la clause d’expéditeurs approuvés de la condition de règle de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="27b84-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="27b84-119">Si cette propriété est 0, aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="27b84-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27b84-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="27b84-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27b84-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="27b84-121">Protocol specifications</span></span>

<span data-ttu-id="27b84-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27b84-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27b84-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="27b84-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27b84-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27b84-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27b84-125">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="27b84-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27b84-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="27b84-126">Header files</span></span>

<span data-ttu-id="27b84-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27b84-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="27b84-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27b84-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="27b84-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="27b84-129">Mapitags.h</span></span>
  
> <span data-ttu-id="27b84-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="27b84-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27b84-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27b84-131">See also</span></span>



[<span data-ttu-id="27b84-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27b84-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27b84-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27b84-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27b84-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27b84-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27b84-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="27b84-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

