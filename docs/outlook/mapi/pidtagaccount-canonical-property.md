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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785673"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="75a27-103">Propriété canonique PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="75a27-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="75a27-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75a27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75a27-105">Contient le nom du compte du destinataire.</span><span class="sxs-lookup"><span data-stu-id="75a27-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75a27-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="75a27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75a27-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="75a27-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="75a27-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="75a27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75a27-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="75a27-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="75a27-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="75a27-110">Data type:</span></span>  <br/> |<span data-ttu-id="75a27-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75a27-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="75a27-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="75a27-112">Area:</span></span>  <br/> |<span data-ttu-id="75a27-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="75a27-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75a27-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="75a27-114">Remarks</span></span>

<span data-ttu-id="75a27-115">Ces propriétés permettent d’identifier et accéder aux informations pour un destinataire.</span><span class="sxs-lookup"><span data-stu-id="75a27-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="75a27-116">Ils sont définis par le destinataire et de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="75a27-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="75a27-117">Ces propriétés couramment contiennent du nom de messagerie du destinataire, autrement dit, le dernier composant de l’adresse de messagerie, qui identifie le destinataire dans l’organisation locale.</span><span class="sxs-lookup"><span data-stu-id="75a27-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="75a27-118">L’adresse de messagerie correspond au nom unique X.400, qui est supposé être un nom court uniques au sein d’un certain domaine de messagerie.</span><span class="sxs-lookup"><span data-stu-id="75a27-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75a27-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="75a27-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75a27-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="75a27-120">Protocol specifications</span></span>

<span data-ttu-id="75a27-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a27-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a27-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="75a27-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75a27-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a27-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a27-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="75a27-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="75a27-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a27-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a27-126">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="75a27-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75a27-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="75a27-127">Header files</span></span>

<span data-ttu-id="75a27-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="75a27-128">mapitags.h</span></span>
  
> <span data-ttu-id="75a27-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="75a27-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="75a27-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75a27-130">mapidefs.h</span></span>
  
> <span data-ttu-id="75a27-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="75a27-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75a27-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75a27-132">See also</span></span>



[<span data-ttu-id="75a27-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75a27-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="75a27-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="75a27-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75a27-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="75a27-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75a27-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="75a27-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

