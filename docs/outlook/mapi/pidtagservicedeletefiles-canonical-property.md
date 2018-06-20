---
title: Propriété canonique PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786790"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="0ce7b-103">Propriété canonique PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="0ce7b-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="0ce7b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ce7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ce7b-105">Contient une liste des noms de fichiers qui doivent être supprimées lors de la désinstallation du service de message.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce7b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0ce7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ce7b-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="0ce7b-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="0ce7b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0ce7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ce7b-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="0ce7b-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="0ce7b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0ce7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ce7b-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ce7b-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0ce7b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0ce7b-112">Area:</span></span>  <br/> |<span data-ttu-id="0ce7b-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce7b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ce7b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ce7b-114">Remarks</span></span>

<span data-ttu-id="0ce7b-115">Les noms de fichiers dans la liste contenue dans ces propriétés sont supprimés de l’ordinateur lorsque vous utilisez le panneau de configuration pour désinstaller le service de message.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="0ce7b-116">N’incluez pas dans la liste des DLL qui prend en charge de plusieurs services de messagerie ou services de messagerie supplémentaires peuvent être supprimés par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="0ce7b-117">MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="0ce7b-118">Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ce7b-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0ce7b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0ce7b-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0ce7b-120">Header files</span></span>

<span data-ttu-id="0ce7b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ce7b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ce7b-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ce7b-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0ce7b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0ce7b-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0ce7b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ce7b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce7b-125">See also</span></span>



[<span data-ttu-id="0ce7b-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce7b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ce7b-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce7b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ce7b-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce7b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ce7b-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0ce7b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

