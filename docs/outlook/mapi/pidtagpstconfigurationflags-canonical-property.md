---
title: Propriété canonique PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786467"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="25b70-103">Propriété canonique PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="25b70-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="25b70-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25b70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25b70-105">Spécifie les indicateurs de configuration pour une table de stockage personnel (fichier .pst).</span><span class="sxs-lookup"><span data-stu-id="25b70-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25b70-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25b70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25b70-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="25b70-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="25b70-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25b70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25b70-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="25b70-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="25b70-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25b70-110">Data type:</span></span>  <br/> |<span data-ttu-id="25b70-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25b70-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25b70-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="25b70-112">Area:</span></span>  <br/> |<span data-ttu-id="25b70-113">Tableau de stockage personnel (.pst) interne</span><span class="sxs-lookup"><span data-stu-id="25b70-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25b70-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25b70-114">Remarks</span></span>

<span data-ttu-id="25b70-115">Les valeurs valides pour cette propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="25b70-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="25b70-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25b70-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="25b70-117">Indique un fichier .pst Unicode.</span><span class="sxs-lookup"><span data-stu-id="25b70-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="25b70-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="25b70-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="25b70-119">Lorsque set à partir du client indicateurs à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , **ConfigureMsgService** la traite comme un appel [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore la « ce service d’informations n'a pas été configuré » avertissement.</span><span class="sxs-lookup"><span data-stu-id="25b70-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="25b70-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="25b70-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="25b70-121">Indique à **ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie.</span><span class="sxs-lookup"><span data-stu-id="25b70-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="25b70-122">Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers .pst.</span><span class="sxs-lookup"><span data-stu-id="25b70-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="25b70-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="25b70-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="25b70-124">Indique le code de configuration pour la première afficher une boîte de dialogue pour vérifier si un fichier de dossier hors connexion (.ost) a été trouvé et, en fonction de la réponse de l’utilisateur, utiliser le dossier en mode hors connexion trouvé ou permettre à l’utilisateur rechercher un autre dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="25b70-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="25b70-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="25b70-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="25b70-126">Copie du fichier .ost avec un nouveau nom unique et ignore le nom actuel.</span><span class="sxs-lookup"><span data-stu-id="25b70-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="25b70-127">Le fichier .ost existant reste sur l’ordinateur, mais n’est plus utilisé dans ce profil.</span><span class="sxs-lookup"><span data-stu-id="25b70-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="25b70-128">Cela se produit généralement lorsque Microsoft Outlook ne sont plus permet à un fichier .ost particulier et stratégies de Registre ne pas autorisent l’utilisateur à renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="25b70-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="25b70-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25b70-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25b70-130">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="25b70-130">Protocol specifications</span></span>

<span data-ttu-id="25b70-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="25b70-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="25b70-132">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="25b70-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25b70-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25b70-133">Header files</span></span>

<span data-ttu-id="25b70-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25b70-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="25b70-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25b70-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="25b70-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="25b70-136">Mapitags.h</span></span>
  
> <span data-ttu-id="25b70-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="25b70-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25b70-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25b70-138">See also</span></span>



[<span data-ttu-id="25b70-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25b70-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25b70-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25b70-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25b70-141">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25b70-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25b70-142">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="25b70-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

