---
title: Propriété canonique PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329392"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="b6b4c-103">Propriété canonique PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="b6b4c-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="b6b4c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b4c-105">Spécifie le serveur qu’un client tente actuellement d’utiliser pour envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b4c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b6b4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6b4c-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="b6b4c-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="b6b4c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b6b4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6b4c-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="b6b4c-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="b6b4c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b6b4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6b4c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6b4c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b6b4c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b6b4c-112">Area:</span></span>  <br/> |<span data-ttu-id="b6b4c-113">Outlook application</span><span class="sxs-lookup"><span data-stu-id="b6b4c-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6b4c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6b4c-114">Remarks</span></span>

<span data-ttu-id="b6b4c-115">Le format de cette propriété dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="b6b4c-116">Cette propriété peut être utilisée par le client pour déterminer le serveur vers lequel diriger le courrier électronique, mais elle est facultative et la valeur n’a aucune signification pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6b4c-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b6b4c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6b4c-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b6b4c-118">Protocol specifications</span></span>

<span data-ttu-id="b6b4c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b4c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b4c-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6b4c-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b4c-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b4c-122">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b6b4c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6b4c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6b4c-124">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6b4c-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b6b4c-125">Header files</span></span>

<span data-ttu-id="b6b4c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6b4c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6b4c-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6b4c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b6b4c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b6b4c-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b6b4c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6b4c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6b4c-130">See also</span></span>



[<span data-ttu-id="b6b4c-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b4c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6b4c-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b4c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6b4c-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b4c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6b4c-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b6b4c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

