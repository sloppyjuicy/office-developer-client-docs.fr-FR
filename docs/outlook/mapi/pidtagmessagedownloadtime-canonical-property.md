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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786226"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="700eb-103">Propriété canonique PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="700eb-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="700eb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="700eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="700eb-105">Contient la durée estimée pour télécharger un message à partir d’un serveur distant sur une banque de messages locale.</span><span class="sxs-lookup"><span data-stu-id="700eb-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="700eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="700eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="700eb-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="700eb-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="700eb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="700eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="700eb-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="700eb-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="700eb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="700eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="700eb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="700eb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="700eb-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="700eb-112">Area:</span></span>  <br/> |<span data-ttu-id="700eb-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="700eb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="700eb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="700eb-114">Remarks</span></span>

<span data-ttu-id="700eb-115">Cette propriété est exprimée en secondes et constitue la meilleure estimation du temps qu’il faudrait un fournisseur de transport à distance pour télécharger un message donné à partir de son emplacement actuel sur une banque de messages local pour le client affichant le dossier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="700eb-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="700eb-116">Le fournisseur de transport à distance calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse de la liaison de communication en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="700eb-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="700eb-117">Si le fournisseur ne peut pas calculer le temps de téléchargement, par exemple, si elle ne sait pas la vitesse de la liaison, il doit fournir une valeur **PT_ERROR** comme **MAPI_E_NO_SUPPORT** pour cette colonne dans le tableau contenu de dossier en-tête.</span><span class="sxs-lookup"><span data-stu-id="700eb-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="700eb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="700eb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="700eb-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="700eb-119">Header files</span></span>

<span data-ttu-id="700eb-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="700eb-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="700eb-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="700eb-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="700eb-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="700eb-122">Mapitags.h</span></span>
  
> <span data-ttu-id="700eb-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="700eb-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="700eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="700eb-124">See also</span></span>



[<span data-ttu-id="700eb-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="700eb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="700eb-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="700eb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="700eb-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="700eb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="700eb-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="700eb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

