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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286407"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="3deb8-103">Propriété canonique PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="3deb8-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="3deb8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3deb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3deb8-105">Indicateurs de configuration spécifie pour une table de stockage personnelle (fichier. pst).</span><span class="sxs-lookup"><span data-stu-id="3deb8-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3deb8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3deb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3deb8-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3deb8-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3deb8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3deb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3deb8-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="3deb8-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="3deb8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3deb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="3deb8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3deb8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3deb8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3deb8-112">Area:</span></span>  <br/> |<span data-ttu-id="3deb8-113">Table de stockage personnel (. pst) interne</span><span class="sxs-lookup"><span data-stu-id="3deb8-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3deb8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3deb8-114">Remarks</span></span>

<span data-ttu-id="3deb8-115">Les valeurs valides pour cette propriété sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="3deb8-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="3deb8-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3deb8-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="3deb8-117">Indique un fichier. PST Unicode.</span><span class="sxs-lookup"><span data-stu-id="3deb8-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="3deb8-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="3deb8-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="3deb8-119">Lorsqu'il est défini à partir des indicateurs client sur la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , traite **ConfigureMsgService** comme un appel [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore le message d'information «ce service d'information n'a pas été configuré» message.</span><span class="sxs-lookup"><span data-stu-id="3deb8-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="3deb8-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="3deb8-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="3deb8-121">Indique à **ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie.</span><span class="sxs-lookup"><span data-stu-id="3deb8-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="3deb8-122">Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers. pst.</span><span class="sxs-lookup"><span data-stu-id="3deb8-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="3deb8-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="3deb8-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="3deb8-124">Indique au code de configuration d'afficher d'abord une boîte de dialogue pour vérifier si un fichier de dossiers en mode hors connexion (. ost) a été trouvé et, en fonction de la réponse de l'utilisateur, utiliser le dossier en mode hors connexion trouvé ou permettre à l'utilisateur de rechercher un autre dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3deb8-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="3deb8-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3deb8-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="3deb8-126">Copie le fichier. ost avec un nouveau nom unique et ignore le nom actuel.</span><span class="sxs-lookup"><span data-stu-id="3deb8-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="3deb8-127">Le fichier. ost existant reste sur l'ordinateur, mais n'est plus utilisé dans ce profil.</span><span class="sxs-lookup"><span data-stu-id="3deb8-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="3deb8-128">Cela se produit généralement lorsque Microsoft Outlook n'autorise plus un fichier. ost particulier et que les stratégies de registre ne permettent pas à l'utilisateur de renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="3deb8-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="3deb8-129">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="3deb8-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3deb8-130">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3deb8-130">Protocol specifications</span></span>

<span data-ttu-id="3deb8-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3deb8-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3deb8-132">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3deb8-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3deb8-133">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3deb8-133">Header files</span></span>

<span data-ttu-id="3deb8-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3deb8-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3deb8-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3deb8-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3deb8-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3deb8-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3deb8-137">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3deb8-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3deb8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3deb8-138">See also</span></span>



[<span data-ttu-id="3deb8-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3deb8-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3deb8-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3deb8-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3deb8-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3deb8-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3deb8-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3deb8-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

