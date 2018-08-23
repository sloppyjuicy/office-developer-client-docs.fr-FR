---
title: Propriété canonique PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 55da942e59c619dd384bef58349aa3a00d4a6d8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571471"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="25ac5-103">Propriété canonique PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="25ac5-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="25ac5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25ac5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25ac5-105">Contient une valeur de redondance cyclique (CRC) sur le texte du message.</span><span class="sxs-lookup"><span data-stu-id="25ac5-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25ac5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25ac5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25ac5-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="25ac5-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="25ac5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25ac5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25ac5-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="25ac5-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="25ac5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25ac5-110">Data type:</span></span>  <br/> |<span data-ttu-id="25ac5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25ac5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25ac5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="25ac5-112">Area:</span></span>  <br/> |<span data-ttu-id="25ac5-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="25ac5-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25ac5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25ac5-114">Remarks</span></span>

<span data-ttu-id="25ac5-115">La banque de messages permettre utiliser n’importe quel algorithme CRC qui génère une valeur PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="25ac5-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="25ac5-116">Il doit calculer cette propriété dans le cadre de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) lorsque la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) a été définie pour la première fois, et chaque fois qu’il a été modifié par la suite.</span><span class="sxs-lookup"><span data-stu-id="25ac5-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="25ac5-117">Une application cliente utilise **PR_BODY_CRC** pour faciliter la comparaison de chaînes de texte de message contenues dans les propriétés **PR_BODY** ou leurs variantes.</span><span class="sxs-lookup"><span data-stu-id="25ac5-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="25ac5-118">À l’aide de cette propriété, le client peut rapidement et facilement détecter lorsque le texte du message a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="25ac5-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="25ac5-119">Il peut réaliser des gains de performances significatifs en utilisant **PR_BODY_CRC** au lieu d’obtention **PR_BODY** à partir de la banque de messages et en les comparant avec une version locale.</span><span class="sxs-lookup"><span data-stu-id="25ac5-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25ac5-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25ac5-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="25ac5-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25ac5-121">Header files</span></span>

<span data-ttu-id="25ac5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25ac5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="25ac5-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25ac5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="25ac5-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="25ac5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="25ac5-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="25ac5-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25ac5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ac5-126">See also</span></span>



[<span data-ttu-id="25ac5-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25ac5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25ac5-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25ac5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25ac5-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25ac5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25ac5-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="25ac5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

