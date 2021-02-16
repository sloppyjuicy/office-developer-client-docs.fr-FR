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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358533"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="71021-103">Propriété canonique PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="71021-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="71021-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71021-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71021-105">Contient TRUE lorsque la pièce jointe représente un autre réplica.</span><span class="sxs-lookup"><span data-stu-id="71021-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71021-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="71021-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71021-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="71021-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="71021-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="71021-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71021-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="71021-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="71021-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="71021-110">Data type:</span></span>  <br/> |<span data-ttu-id="71021-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="71021-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="71021-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="71021-112">Area:</span></span>  <br/> |<span data-ttu-id="71021-113">Note de conflit</span><span class="sxs-lookup"><span data-stu-id="71021-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71021-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="71021-114">Remarks</span></span>

<span data-ttu-id="71021-115">Le client et le serveur de messagerie doivent générer un message de résolution de conflit lors de la détection d’un conflit avec la version actuelle d’un message dans le réplica lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="71021-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="71021-116">Il est important de comprendre qu’il est possible que la version actuelle du message dans le réplica local a été transmise pendant l’opération de synchronisation en cours.</span><span class="sxs-lookup"><span data-stu-id="71021-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="71021-117">Cela se produit lorsque le conflit existe déjà sur le serveur avant le téléchargement de l’un des messages en conflit vers le réplica local.</span><span class="sxs-lookup"><span data-stu-id="71021-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="71021-118">Un message de résolution de conflit doit être synchronisé en tant que réplicas indépendants avec des PCL en conflit.</span><span class="sxs-lookup"><span data-stu-id="71021-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="71021-119">Le message de résolution de conflit lui-même ne doit pas être synchronisé entre le client et le serveur ; seuls les réplicas indépendants doivent être échangés.</span><span class="sxs-lookup"><span data-stu-id="71021-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="71021-120">Le partenaire de synchronisation doit ensuite générer un nouveau message qui correspond à la structure du message en conflit.</span><span class="sxs-lookup"><span data-stu-id="71021-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="71021-121">Par conséquent, il est important que le client et le serveur utilisent le même algorithme pour détecter l’élément « gagne ».</span><span class="sxs-lookup"><span data-stu-id="71021-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="71021-122">Les règles suivantes doivent être appliquées pour détecter le « gagneur » :</span><span class="sxs-lookup"><span data-stu-id="71021-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="71021-123">Heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="71021-123">Last modification time.</span></span>
    
2. <span data-ttu-id="71021-124">GUID CN supérieur (à l’aide de la comparaison de mémoire) pour rompre l’égalité.</span><span class="sxs-lookup"><span data-stu-id="71021-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="71021-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="71021-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71021-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="71021-126">Protocol specifications</span></span>

<span data-ttu-id="71021-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71021-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71021-128">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="71021-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71021-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71021-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71021-130">Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="71021-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71021-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="71021-131">Header files</span></span>

<span data-ttu-id="71021-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71021-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="71021-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="71021-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="71021-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71021-134">Mapitags.h</span></span>
  
> <span data-ttu-id="71021-135">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="71021-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71021-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71021-136">See also</span></span>



[<span data-ttu-id="71021-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="71021-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71021-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="71021-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71021-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="71021-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71021-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="71021-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

