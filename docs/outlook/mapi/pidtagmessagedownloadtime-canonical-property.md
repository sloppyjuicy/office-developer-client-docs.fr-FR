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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325675"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="f520e-103">Propriété canonique PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="f520e-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="f520e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f520e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f520e-105">Contient la durée estimée de téléchargement d'un message à partir d'un serveur distant vers une banque de messages locale.</span><span class="sxs-lookup"><span data-stu-id="f520e-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f520e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f520e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f520e-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="f520e-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="f520e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f520e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f520e-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="f520e-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="f520e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f520e-110">Data type:</span></span>  <br/> |<span data-ttu-id="f520e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f520e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f520e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f520e-112">Area:</span></span>  <br/> |<span data-ttu-id="f520e-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="f520e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f520e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f520e-114">Remarks</span></span>

<span data-ttu-id="f520e-115">Cette propriété est exprimée en secondes et représente la meilleure estimation du temps qu'un fournisseur de transport distant doit prendre pour télécharger un message donné à partir de son emplacement actuel vers un magasin de messages local sur le client en affichant le dossier d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="f520e-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="f520e-116">Le fournisseur de transport distant calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse du lien de communication en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="f520e-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="f520e-117">Si le fournisseur ne peut pas calculer le temps de téléchargement, par exemple s'il ne connaît pas la vitesse de la liaison, il doit fournir une valeur **PT_ERROR** telle que **MAPI_E_NO_SUPPORT** pour cette colonne dans le tableau des matières du dossier d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="f520e-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f520e-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f520e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f520e-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f520e-119">Header files</span></span>

<span data-ttu-id="f520e-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f520e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f520e-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f520e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f520e-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f520e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f520e-123">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f520e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f520e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f520e-124">See also</span></span>



[<span data-ttu-id="f520e-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f520e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f520e-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f520e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f520e-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f520e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f520e-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f520e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

