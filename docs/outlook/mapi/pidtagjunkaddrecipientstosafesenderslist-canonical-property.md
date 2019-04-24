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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3a87beaa3873b5ccb449e5b1497262bad5bf1497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282367"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="a9a46-103">Propriété canonique PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="a9a46-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="a9a46-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9a46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9a46-105">Indique si les destinataires de messagerie doivent être ajoutés à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="a9a46-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9a46-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a9a46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9a46-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="a9a46-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="a9a46-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a9a46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9a46-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="a9a46-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="a9a46-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a9a46-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9a46-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a9a46-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a9a46-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a9a46-112">Area:</span></span>  <br/> |<span data-ttu-id="a9a46-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a9a46-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9a46-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a9a46-114">Remarks</span></span>

<span data-ttu-id="a9a46-115">S'il est présent, cette propriété doit être définie sur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="a9a46-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="a9a46-116">La valeur 1 indique que les destinataires de courrier doivent être ajoutés à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="a9a46-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="a9a46-117">La valeur 0 indique que les destinataires ne doivent pas être ajoutés à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="a9a46-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="a9a46-118">Si cette propriété est présente avec une valeur de 1, les adresses SMTP des destinataires du courrier électronique doivent être ajoutées à la clause des expéditeurs approuvés de la condition de règle de courrier inDésirable.</span><span class="sxs-lookup"><span data-stu-id="a9a46-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="a9a46-119">Si cette propriété a la valeur 0, aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="a9a46-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9a46-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a9a46-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9a46-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a9a46-121">Protocol specifications</span></span>

<span data-ttu-id="a9a46-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9a46-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9a46-123">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a9a46-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9a46-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9a46-124">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9a46-125">Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="a9a46-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9a46-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a9a46-126">Header files</span></span>

<span data-ttu-id="a9a46-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a9a46-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9a46-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a9a46-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9a46-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a9a46-129">Mapitags.h</span></span>
  
> <span data-ttu-id="a9a46-130">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="a9a46-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9a46-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9a46-131">See also</span></span>



[<span data-ttu-id="a9a46-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a9a46-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9a46-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a9a46-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9a46-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a9a46-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9a46-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a9a46-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

