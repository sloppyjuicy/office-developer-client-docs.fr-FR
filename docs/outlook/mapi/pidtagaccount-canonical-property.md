---
title: Propriété canonique PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401103"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="9cf7f-103">Propriété canonique PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="9cf7f-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="9cf7f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cf7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cf7f-105">Contient le nom du compte du destinataire.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cf7f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9cf7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cf7f-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="9cf7f-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="9cf7f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9cf7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cf7f-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="9cf7f-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="9cf7f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9cf7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cf7f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9cf7f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9cf7f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9cf7f-112">Area:</span></span>  <br/> |<span data-ttu-id="9cf7f-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="9cf7f-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cf7f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cf7f-114">Remarks</span></span>

<span data-ttu-id="9cf7f-115">Ces propriétés permettent d’identifier et accéder aux informations pour un destinataire.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="9cf7f-116">Ils sont définis par le destinataire et de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="9cf7f-117">Ces propriétés couramment contiennent du nom de messagerie du destinataire, autrement dit, le dernier composant de l’adresse de messagerie, qui identifie le destinataire dans l’organisation locale.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="9cf7f-118">L’adresse de messagerie correspond au nom unique X.400, qui est supposé être un nom court uniques au sein d’un certain domaine de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9cf7f-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9cf7f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cf7f-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9cf7f-120">Protocol specifications</span></span>

<span data-ttu-id="9cf7f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cf7f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cf7f-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cf7f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cf7f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cf7f-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="9cf7f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cf7f-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cf7f-126">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cf7f-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9cf7f-127">Header files</span></span>

<span data-ttu-id="9cf7f-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9cf7f-128">mapitags.h</span></span>
  
> <span data-ttu-id="9cf7f-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="9cf7f-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cf7f-130">mapidefs.h</span></span>
  
> <span data-ttu-id="9cf7f-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cf7f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cf7f-132">See also</span></span>



[<span data-ttu-id="9cf7f-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9cf7f-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="9cf7f-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9cf7f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cf7f-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9cf7f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cf7f-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9cf7f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

