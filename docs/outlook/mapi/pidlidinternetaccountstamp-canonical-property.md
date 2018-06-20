---
title: Propriété canonique PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 49732f30461e05e83c130f9cc24129cc86baa75f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785259"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="80125-103">Propriété canonique PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="80125-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="80125-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80125-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80125-105">Spécifie l’ID de compte de messagerie à travers lequel le message électronique est envoyé.</span><span class="sxs-lookup"><span data-stu-id="80125-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80125-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="80125-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80125-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="80125-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="80125-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="80125-108">Property set:</span></span>  <br/> |<span data-ttu-id="80125-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="80125-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="80125-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="80125-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="80125-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="80125-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="80125-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="80125-112">Data type:</span></span>  <br/> |<span data-ttu-id="80125-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80125-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="80125-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="80125-114">Area:</span></span>  <br/> |<span data-ttu-id="80125-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="80125-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80125-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="80125-116">Remarks</span></span>

<span data-ttu-id="80125-117">Le format de cette chaîne est dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="80125-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="80125-118">Cette propriété peut être utilisée par le client pour déterminer le serveur pour diriger la messagerie, mais est facultative et la valeur est dépourvu de signification sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="80125-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80125-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="80125-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80125-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="80125-120">Protocol specifications</span></span>

<span data-ttu-id="80125-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80125-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80125-122">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="80125-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80125-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80125-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80125-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="80125-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80125-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="80125-125">Header files</span></span>

<span data-ttu-id="80125-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80125-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="80125-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="80125-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80125-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80125-128">See also</span></span>



[<span data-ttu-id="80125-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="80125-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80125-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="80125-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80125-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="80125-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80125-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="80125-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

