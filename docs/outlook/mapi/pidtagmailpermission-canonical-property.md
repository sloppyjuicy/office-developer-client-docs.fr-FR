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
ms.openlocfilehash: 4cc97647c60322783050abbebd18726434632a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786206"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="0c566-103">Propriété canonique PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="0c566-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="0c566-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c566-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c566-105">Contient la valeur TRUE si l’utilisateur de messagerie est autorisé à envoyer et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="0c566-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c566-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0c566-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c566-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="0c566-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="0c566-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0c566-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c566-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="0c566-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="0c566-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0c566-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c566-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0c566-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0c566-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0c566-112">Area:</span></span>  <br/> |<span data-ttu-id="0c566-113">Address</span><span class="sxs-lookup"><span data-stu-id="0c566-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c566-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c566-114">Remarks</span></span>

<span data-ttu-id="0c566-115">Si cette propriété n’est pas définie, MAPI la traite comme ayant la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="0c566-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="0c566-116">Définir cette propriété sur FALSE dans un annuaire d’entreprise où certaines entrées ne sont pas à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="0c566-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0c566-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0c566-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0c566-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0c566-118">Header files</span></span>

<span data-ttu-id="0c566-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c566-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c566-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0c566-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c566-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0c566-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0c566-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0c566-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c566-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c566-123">See also</span></span>



[<span data-ttu-id="0c566-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0c566-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c566-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0c566-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c566-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0c566-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c566-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0c566-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

