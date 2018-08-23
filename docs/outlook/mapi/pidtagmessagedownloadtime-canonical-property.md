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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 43916f540ca324059d53f0413105146985835ffe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588698"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="53c66-103">Propriété canonique PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="53c66-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="53c66-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53c66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53c66-105">Contient la durée estimée pour télécharger un message à partir d’un serveur distant sur une banque de messages locale.</span><span class="sxs-lookup"><span data-stu-id="53c66-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53c66-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="53c66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53c66-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="53c66-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="53c66-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="53c66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53c66-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="53c66-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="53c66-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="53c66-110">Data type:</span></span>  <br/> |<span data-ttu-id="53c66-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53c66-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="53c66-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="53c66-112">Area:</span></span>  <br/> |<span data-ttu-id="53c66-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="53c66-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53c66-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="53c66-114">Remarks</span></span>

<span data-ttu-id="53c66-115">Cette propriété est exprimée en secondes et constitue la meilleure estimation du temps qu’il faudrait un fournisseur de transport à distance pour télécharger un message donné à partir de son emplacement actuel sur une banque de messages local pour le client affichant le dossier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="53c66-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="53c66-116">Le fournisseur de transport à distance calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse de la liaison de communication en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="53c66-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="53c66-117">Si le fournisseur ne peut pas calculer le temps de téléchargement, par exemple, si elle ne sait pas la vitesse de la liaison, il doit fournir une valeur **PT_ERROR** comme **MAPI_E_NO_SUPPORT** pour cette colonne dans le tableau contenu de dossier en-tête.</span><span class="sxs-lookup"><span data-stu-id="53c66-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="53c66-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="53c66-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="53c66-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="53c66-119">Header files</span></span>

<span data-ttu-id="53c66-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53c66-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="53c66-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="53c66-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="53c66-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="53c66-122">Mapitags.h</span></span>
  
> <span data-ttu-id="53c66-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="53c66-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53c66-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c66-124">See also</span></span>



[<span data-ttu-id="53c66-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="53c66-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53c66-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="53c66-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53c66-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="53c66-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53c66-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="53c66-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

