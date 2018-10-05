---
title: Propriété canonique PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384436"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="3d951-103">Propriété canonique PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="3d951-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="3d951-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d951-105">Contient la valeur TRUE lorsque la pièce jointe représente un autre réplica.</span><span class="sxs-lookup"><span data-stu-id="3d951-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d951-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3d951-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d951-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="3d951-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="3d951-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3d951-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d951-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="3d951-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="3d951-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3d951-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d951-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3d951-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3d951-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3d951-112">Area:</span></span>  <br/> |<span data-ttu-id="3d951-113">Note de conflit</span><span class="sxs-lookup"><span data-stu-id="3d951-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d951-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d951-114">Remarks</span></span>

<span data-ttu-id="3d951-115">Le client de messagerie et le serveur doivent générer un message de résolution de conflit lors de la détection de conflit par rapport à la version actuelle d’un message dans le réplica lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3d951-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="3d951-116">Il est important de comprendre qu’il est possible que la version actuelle du message dans le réplica local a été transmise au cours de l’opération en cours de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3d951-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="3d951-117">Cela se produit lorsque le conflit existe déjà sur le serveur avant d’un des messages en conflit ont été téléchargé sur le réplica local.</span><span class="sxs-lookup"><span data-stu-id="3d951-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="3d951-118">Un conflit de résoudre le message doit être synchronisé en tant que réplicas indépendants avec PCLs en conflit.</span><span class="sxs-lookup"><span data-stu-id="3d951-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="3d951-119">Résoudre le conflit le message lui-même ne doit pas être synchronisée entre client et serveur ; uniquement les réplicas indépendantes doivent être échangés.</span><span class="sxs-lookup"><span data-stu-id="3d951-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="3d951-120">Le partenaire de synchronisation doit ensuite générer un nouveau message qui correspond à la structure du message de conflit.</span><span class="sxs-lookup"><span data-stu-id="3d951-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="3d951-121">Par conséquent, il est important que client et serveur utilisent le même algorithme pour détecter l’élément « prix ».</span><span class="sxs-lookup"><span data-stu-id="3d951-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="3d951-122">Les règles suivantes doivent être appliquées pour détecter le « prix » :</span><span class="sxs-lookup"><span data-stu-id="3d951-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="3d951-123">Heure de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="3d951-123">Last modification time.</span></span>
    
2. <span data-ttu-id="3d951-124">Supérieur CN GUID (à l’aide de la comparaison de la mémoire) pour rompre papillon.</span><span class="sxs-lookup"><span data-stu-id="3d951-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3d951-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3d951-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d951-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3d951-126">Protocol specifications</span></span>

<span data-ttu-id="3d951-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d951-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d951-128">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3d951-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d951-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d951-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d951-130">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="3d951-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d951-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3d951-131">Header files</span></span>

<span data-ttu-id="3d951-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d951-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d951-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3d951-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d951-134">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3d951-134">Mapitags.h</span></span>
  
> <span data-ttu-id="3d951-135">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3d951-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d951-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d951-136">See also</span></span>



[<span data-ttu-id="3d951-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3d951-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d951-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3d951-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d951-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3d951-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d951-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3d951-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

