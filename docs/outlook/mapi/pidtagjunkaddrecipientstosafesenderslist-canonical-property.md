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
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786153"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a><span data-ttu-id="53d23-103">Propriété canonique PidTagJunkAddRecipientsToSafeSendersList</span><span class="sxs-lookup"><span data-stu-id="53d23-103">PidTagJunkAddRecipientsToSafeSendersList Canonical Property</span></span>

  
  
<span data-ttu-id="53d23-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53d23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53d23-105">Indique si les destinataires de messagerie à ajouter à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="53d23-105">Indicates whether or not the mail recipients are to be added to the safe senders list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53d23-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="53d23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53d23-107">PR_JUNK_ADD_RECIPS_TO_SSL</span><span class="sxs-lookup"><span data-stu-id="53d23-107">PR_JUNK_ADD_RECIPS_TO_SSL</span></span>  <br/> |
|<span data-ttu-id="53d23-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="53d23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53d23-109">0x6103</span><span class="sxs-lookup"><span data-stu-id="53d23-109">0x6103</span></span>  <br/> |
|<span data-ttu-id="53d23-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="53d23-110">Data type:</span></span>  <br/> |<span data-ttu-id="53d23-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53d23-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="53d23-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="53d23-112">Area:</span></span>  <br/> |<span data-ttu-id="53d23-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="53d23-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53d23-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="53d23-114">Remarks</span></span>

<span data-ttu-id="53d23-115">Le cas échéant, cette propriété doit être définie sur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="53d23-115">If present, this property must be set to 0 or 1.</span></span> <span data-ttu-id="53d23-116">Une valeur de 1 indique que les destinataires de messagerie sont à ajouter à la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="53d23-116">A value of 1 indicates that the mail recipients are to be added to the safe senders list.</span></span> <span data-ttu-id="53d23-117">Une valeur de 0 indique que les destinataires de messagerie ne doivent ne pas figurer dans la liste des expéditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="53d23-117">A value of 0 indicates that the mail recipients are not to be added to the safe senders list.</span></span>
  
<span data-ttu-id="53d23-118">Si cette propriété est présente avec la valeur 1, les adresses SMTP des destinataires de courrier électronique doivent être ajoutés à la clause d’expéditeurs approuvés de la condition de règle de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="53d23-118">If this property is present with a value of 1, the SMTP addresses of the email recipients must be added to trusted senders clause of the Junk E-Mail Rule condition.</span></span> <span data-ttu-id="53d23-119">Si cette propriété est 0, aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="53d23-119">If this property is 0, no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53d23-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="53d23-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53d23-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="53d23-121">Protocol specifications</span></span>

<span data-ttu-id="53d23-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53d23-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53d23-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="53d23-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53d23-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53d23-124">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53d23-125">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="53d23-125">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53d23-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="53d23-126">Header files</span></span>

<span data-ttu-id="53d23-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53d23-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="53d23-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="53d23-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="53d23-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="53d23-129">Mapitags.h</span></span>
  
> <span data-ttu-id="53d23-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="53d23-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53d23-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53d23-131">See also</span></span>



[<span data-ttu-id="53d23-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="53d23-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53d23-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="53d23-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53d23-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="53d23-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53d23-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="53d23-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

