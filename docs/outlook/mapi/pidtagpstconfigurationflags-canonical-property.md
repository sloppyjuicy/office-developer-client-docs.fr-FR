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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408942"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="ff54c-103">Propriété canonique PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="ff54c-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="ff54c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff54c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff54c-105">Spécifications des indicateurs de configuration pour une table de stockage personnel (fichier .pst).</span><span class="sxs-lookup"><span data-stu-id="ff54c-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff54c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ff54c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff54c-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ff54c-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ff54c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ff54c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff54c-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="ff54c-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="ff54c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ff54c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff54c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ff54c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ff54c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ff54c-112">Area:</span></span>  <br/> |<span data-ttu-id="ff54c-113">Table de stockage personnel (.pst) interne</span><span class="sxs-lookup"><span data-stu-id="ff54c-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff54c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff54c-114">Remarks</span></span>

<span data-ttu-id="ff54c-115">Les valeurs valides pour cette propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff54c-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="ff54c-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff54c-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="ff54c-117">Indique un fichier .pst Unicode.</span><span class="sxs-lookup"><span data-stu-id="ff54c-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="ff54c-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="ff54c-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="ff54c-119">Lorsqu’il est configuré à partir des indicateurs clients vers la méthode [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) **configureMsgService** est traité comme un appel [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) et ignore l’avertissement « Ce service d’information n’a pas été configuré ».</span><span class="sxs-lookup"><span data-stu-id="ff54c-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="ff54c-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="ff54c-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="ff54c-121">Indique **à ConfigureMsgService** de ne pas modifier la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), même si elle a été fournie.</span><span class="sxs-lookup"><span data-stu-id="ff54c-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="ff54c-122">Dans ce cas, il a été fourni uniquement pour les nouveaux fichiers .pst.</span><span class="sxs-lookup"><span data-stu-id="ff54c-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="ff54c-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="ff54c-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="ff54c-124">Indique au code de configuration d’afficher d’abord une boîte de dialogue pour confirmer si un fichier de dossier hors connexion (.ost) a été trouvé et, selon la réponse de l’utilisateur, utiliser le dossier hors connexion trouvé ou permettre à l’utilisateur de rechercher un autre dossier hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ff54c-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="ff54c-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ff54c-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="ff54c-126">Copie le fichier .ost avec un nouveau nom unique et rejette le nom actuel.</span><span class="sxs-lookup"><span data-stu-id="ff54c-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="ff54c-127">Le fichier .ost existant reste sur l’ordinateur, mais n’est plus utilisé dans ce profil.</span><span class="sxs-lookup"><span data-stu-id="ff54c-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="ff54c-128">Cela se produit généralement lorsque Microsoft Outlook n’autorise plus un fichier .ost particulier et que les stratégies de Registre n’autorisent pas l’utilisateur à renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="ff54c-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="ff54c-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ff54c-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff54c-130">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ff54c-130">Protocol specifications</span></span>

<span data-ttu-id="ff54c-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="ff54c-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="ff54c-132">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="ff54c-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff54c-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ff54c-133">Header files</span></span>

<span data-ttu-id="ff54c-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff54c-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff54c-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ff54c-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff54c-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff54c-136">Mapitags.h</span></span>
  
> <span data-ttu-id="ff54c-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ff54c-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff54c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff54c-138">See also</span></span>



[<span data-ttu-id="ff54c-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ff54c-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff54c-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ff54c-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff54c-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ff54c-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff54c-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ff54c-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

