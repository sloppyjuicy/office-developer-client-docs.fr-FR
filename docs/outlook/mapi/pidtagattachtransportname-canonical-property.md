---
title: Propriété canonique PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400515"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="971ca-103">Propriété canonique PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="971ca-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="971ca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="971ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="971ca-105">Contient le nom d’un fichier de pièce jointe modifié de sorte qu’il peut être associé à des messages TNEF.</span><span class="sxs-lookup"><span data-stu-id="971ca-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="971ca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="971ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="971ca-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="971ca-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="971ca-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="971ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="971ca-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="971ca-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="971ca-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="971ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="971ca-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="971ca-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="971ca-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="971ca-112">Area:</span></span>  <br/> |<span data-ttu-id="971ca-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="971ca-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="971ca-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="971ca-114">Remarks</span></span>

<span data-ttu-id="971ca-115">TNEF et le fournisseur de transport utilisent ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="971ca-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="971ca-116">Ils ne sont généralement pas disponibles pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="971ca-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="971ca-117">Ces propriétés sont couramment utilisées par TNEF lorsque le système de messagerie sous-jacent ne prend pas en charge les noms de fichier fourni.</span><span class="sxs-lookup"><span data-stu-id="971ca-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="971ca-118">Par exemple, ils sont utilisés lorsque l’utilisateur attache plusieurs fichiers portant le même nom, tels que les cinq fichiers nommée CONFIG. SYS.</span><span class="sxs-lookup"><span data-stu-id="971ca-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="971ca-119">Le fournisseur de transport doit modifier les noms pour vous assurer qu’ils sont uniques.</span><span class="sxs-lookup"><span data-stu-id="971ca-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="971ca-120">Chaque nom modifié apparaît dans la pièce jointe **PR_ATTACH_TRANSPORT_NAME** et propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="971ca-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="971ca-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="971ca-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="971ca-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="971ca-122">Protocol specifications</span></span>

<span data-ttu-id="971ca-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="971ca-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="971ca-124">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="971ca-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="971ca-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="971ca-125">Header files</span></span>

<span data-ttu-id="971ca-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="971ca-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="971ca-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="971ca-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="971ca-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="971ca-128">Mapitags.h</span></span>
  
> <span data-ttu-id="971ca-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="971ca-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="971ca-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="971ca-130">See also</span></span>



[<span data-ttu-id="971ca-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="971ca-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="971ca-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="971ca-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="971ca-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="971ca-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="971ca-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="971ca-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

