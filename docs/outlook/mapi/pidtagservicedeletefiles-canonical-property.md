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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436824"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="a7e6d-103">Propriété canonique PidTagServiceDeleteFiles</span><span class="sxs-lookup"><span data-stu-id="a7e6d-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="a7e6d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7e6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7e6d-105">Contient une liste de noms de fichier à supprimer lors de la désinstallation du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7e6d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7e6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7e6d-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="a7e6d-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="a7e6d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a7e6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7e6d-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="a7e6d-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="a7e6d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7e6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7e6d-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7e6d-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a7e6d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a7e6d-112">Area:</span></span>  <br/> |<span data-ttu-id="a7e6d-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e6d-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7e6d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7e6d-114">Remarks</span></span>

<span data-ttu-id="a7e6d-115">Les noms de fichier de la liste contenus dans ces propriétés sont supprimés de l'ordinateur lorsque vous utilisez le panneau de configuration pour désinstaller le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="a7e6d-116">N'incluez pas dans la liste toute DLL qui prend en charge plusieurs services de messagerie ou les services de messages supplémentaires peuvent être supprimés par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="a7e6d-117">MAPI fonctionne uniquement avec les noms de fichier et les autres chaînes qui lui sont transmises, dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="a7e6d-118">Les applications qui utilisent des noms de fichier dans un jeu de caractères OEM doivent les convertir en ANSI avant d'appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7e6d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7e6d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a7e6d-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a7e6d-120">Header files</span></span>

<span data-ttu-id="a7e6d-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a7e6d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7e6d-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7e6d-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a7e6d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a7e6d-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="a7e6d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7e6d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7e6d-125">See also</span></span>



[<span data-ttu-id="a7e6d-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e6d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7e6d-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e6d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7e6d-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7e6d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7e6d-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a7e6d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

