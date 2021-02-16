---
title: Propriété canonique PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339374"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="97896-103">Propriété canonique PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="97896-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="97896-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97896-105">Contient une chaîne qui nomme le premier serveur utilisé pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="97896-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97896-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="97896-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97896-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="97896-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="97896-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="97896-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97896-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="97896-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="97896-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="97896-110">Data type:</span></span>  <br/> |<span data-ttu-id="97896-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97896-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="97896-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="97896-112">Area:</span></span>  <br/> |<span data-ttu-id="97896-113">Compte</span><span class="sxs-lookup"><span data-stu-id="97896-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97896-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="97896-114">Remarks</span></span>

<span data-ttu-id="97896-115">Spécifie le premier serveur qu’un client doit utiliser pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="97896-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="97896-116">Le format de ces propriétés dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="97896-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="97896-117">Ces propriétés peuvent être utilisées par le client pour déterminer le serveur vers lequel diriger le courrier, mais elles sont facultatives et la valeur n’a aucune signification pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="97896-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97896-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="97896-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97896-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="97896-119">Protocol specifications</span></span>

<span data-ttu-id="97896-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97896-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97896-121">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="97896-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97896-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97896-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97896-123">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="97896-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97896-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="97896-124">Header files</span></span>

<span data-ttu-id="97896-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97896-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="97896-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="97896-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="97896-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97896-127">Mapitags.h</span></span>
  
> <span data-ttu-id="97896-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="97896-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97896-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97896-129">See also</span></span>



[<span data-ttu-id="97896-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="97896-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97896-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="97896-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97896-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="97896-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97896-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="97896-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

