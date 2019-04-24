---
title: Propriété canonique PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278871"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="db531-103">Propriété canonique PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="db531-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="db531-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db531-105">Contient la valeur TRUE si l'utilisateur de messagerie est autorisé à envoyer et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="db531-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db531-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="db531-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db531-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="db531-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="db531-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="db531-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db531-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="db531-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="db531-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="db531-110">Data type:</span></span>  <br/> |<span data-ttu-id="db531-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="db531-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="db531-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="db531-112">Area:</span></span>  <br/> |<span data-ttu-id="db531-113">Address</span><span class="sxs-lookup"><span data-stu-id="db531-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db531-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="db531-114">Remarks</span></span>

<span data-ttu-id="db531-115">Si cette propriété n'est pas définie, MAPI la traite comme ayant une valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="db531-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="db531-116">Définissez cette propriété sur FALSe dans un annuaire d'entreprise dans lequel certaines entrées ne sont pas à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="db531-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="db531-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="db531-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="db531-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="db531-118">Header files</span></span>

<span data-ttu-id="db531-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="db531-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="db531-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="db531-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="db531-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="db531-121">Mapitags.h</span></span>
  
> <span data-ttu-id="db531-122">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="db531-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db531-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db531-123">See also</span></span>



[<span data-ttu-id="db531-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="db531-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db531-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="db531-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db531-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="db531-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db531-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="db531-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

