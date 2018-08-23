---
title: Propriété canonique PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5165867e46d3d86d65932e7ae432b446efbd8fff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589125"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="cea87-103">Propriété canonique PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="cea87-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="cea87-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cea87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cea87-105">Contient une liste des fichiers qui appartiennent au service de message.</span><span class="sxs-lookup"><span data-stu-id="cea87-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cea87-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cea87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cea87-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="cea87-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="cea87-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cea87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cea87-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="cea87-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="cea87-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cea87-110">Data type:</span></span>  <br/> |<span data-ttu-id="cea87-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cea87-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cea87-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cea87-112">Area:</span></span>  <br/> |<span data-ttu-id="cea87-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="cea87-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cea87-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cea87-114">Remarks</span></span>

<span data-ttu-id="cea87-115">À l’aide d’une boîte de dialogue dans le panneau, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de message.</span><span class="sxs-lookup"><span data-stu-id="cea87-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="cea87-116">Par exemple, l’utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (DLL) qui appartiennent au service.</span><span class="sxs-lookup"><span data-stu-id="cea87-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="cea87-117">L’utilisateur peut rechercher puis plus d’informations sur les fichiers spécifiés, tels que les noms et les numéros de version de toutes les DLL.</span><span class="sxs-lookup"><span data-stu-id="cea87-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="cea87-118">MAPI utilise ces propriétés pour créer une liste de fichiers de prise en charge dans une boîte de dialogue de sélection de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cea87-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="cea87-119">MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cea87-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="cea87-120">Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="cea87-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cea87-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cea87-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cea87-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cea87-122">Header files</span></span>

<span data-ttu-id="cea87-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cea87-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="cea87-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cea87-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="cea87-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cea87-125">Mapitags.h</span></span>
  
> <span data-ttu-id="cea87-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cea87-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cea87-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cea87-127">See also</span></span>



[<span data-ttu-id="cea87-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cea87-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cea87-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cea87-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cea87-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cea87-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cea87-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cea87-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

