---
title: Propriété canonique PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e67cbb113899487f489ef7235d92d1adfcb76163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563638"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="75ac3-103">Propriété canonique PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="75ac3-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="75ac3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75ac3-105">Contient la valeur de résolution de conflit d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="75ac3-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75ac3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="75ac3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75ac3-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="75ac3-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="75ac3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="75ac3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75ac3-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="75ac3-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="75ac3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="75ac3-110">Data type:</span></span>  <br/> |<span data-ttu-id="75ac3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75ac3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75ac3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="75ac3-112">Area:</span></span>  <br/> |<span data-ttu-id="75ac3-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="75ac3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75ac3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="75ac3-114">Remarks</span></span>

<span data-ttu-id="75ac3-115">Cette propriété sur le dossier contenant le message de résolution de conflit indique comment résoudre le conflit.</span><span class="sxs-lookup"><span data-stu-id="75ac3-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="75ac3-116">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="75ac3-116">This property is not required.</span></span> <span data-ttu-id="75ac3-117">Toutefois, si elle est définie, indicateurs autres que les éléments suivants ne doivent pas être présents :</span><span class="sxs-lookup"><span data-stu-id="75ac3-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75ac3-118">RESOLVE_METHOD_DEFAULT (0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="75ac3-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="75ac3-119">Conflit de résoudre le message doit être généré.</span><span class="sxs-lookup"><span data-stu-id="75ac3-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="75ac3-120">RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="75ac3-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="75ac3-121">Remplacer le message cible avec les dernières modifications seront appliquées.</span><span class="sxs-lookup"><span data-stu-id="75ac3-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="75ac3-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="75ac3-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="75ac3-123">Ne pas envoyer de message de notification de conflit lors de la génération de conflit de résoudre le message dans le dossier public.</span><span class="sxs-lookup"><span data-stu-id="75ac3-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="75ac3-124">Un client ou le serveur ne doit pas générer un message de résolution de conflit pour les messages associés.</span><span class="sxs-lookup"><span data-stu-id="75ac3-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="75ac3-125">Ces messages doivent être résolus à l’aide de la sémantique **RESOLVE_METHOD_LAST_WRITER_WINS** .</span><span class="sxs-lookup"><span data-stu-id="75ac3-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75ac3-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="75ac3-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75ac3-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="75ac3-127">Protocol specifications</span></span>

<span data-ttu-id="75ac3-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75ac3-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75ac3-129">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="75ac3-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="75ac3-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75ac3-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75ac3-131">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="75ac3-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75ac3-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="75ac3-132">Header files</span></span>

<span data-ttu-id="75ac3-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75ac3-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="75ac3-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="75ac3-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="75ac3-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="75ac3-135">Mapitags.h</span></span>
  
> <span data-ttu-id="75ac3-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="75ac3-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75ac3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75ac3-137">See also</span></span>



[<span data-ttu-id="75ac3-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="75ac3-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75ac3-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="75ac3-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75ac3-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="75ac3-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75ac3-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="75ac3-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

