---
title: Propriété canonique PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407927"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="c699d-103">Propriété canonique PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="c699d-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="c699d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c699d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c699d-105">Contient la durée estimée de téléchargement d’un message à partir d’un serveur distant vers un magasin de messages local.</span><span class="sxs-lookup"><span data-stu-id="c699d-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c699d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c699d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c699d-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="c699d-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="c699d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c699d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c699d-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="c699d-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="c699d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c699d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c699d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c699d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c699d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c699d-112">Area:</span></span>  <br/> |<span data-ttu-id="c699d-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="c699d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c699d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c699d-114">Remarks</span></span>

<span data-ttu-id="c699d-115">Cette propriété est exprimée en secondes et représente la meilleure estimation du temps qu’un fournisseur de transport distant doit prendre pour télécharger un message donné à partir de son emplacement actuel vers une boutique de messages locale pour le client qui affiche le dossier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c699d-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="c699d-116">Le fournisseur de transport distant calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse du lien de communication en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="c699d-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="c699d-117">Si le fournisseur ne peut pas calculer la durée de téléchargement, par exemple s’il ne connaît pas la vitesse de liaison, il doit fournir une valeur **PT_ERROR** telle que **MAPI_E_NO_SUPPORT** pour cette colonne dans la table de contenu du dossier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c699d-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c699d-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c699d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c699d-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c699d-119">Header files</span></span>

<span data-ttu-id="c699d-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c699d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c699d-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c699d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c699d-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c699d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c699d-123">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c699d-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c699d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c699d-124">See also</span></span>



[<span data-ttu-id="c699d-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c699d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c699d-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c699d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c699d-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c699d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c699d-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c699d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

