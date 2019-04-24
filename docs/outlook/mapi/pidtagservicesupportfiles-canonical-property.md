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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359471"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="69943-103">Propriété canonique PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="69943-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="69943-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69943-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69943-105">Contient une liste des fichiers qui appartiennent au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="69943-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69943-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="69943-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69943-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="69943-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="69943-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="69943-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69943-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="69943-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="69943-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="69943-110">Data type:</span></span>  <br/> |<span data-ttu-id="69943-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69943-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="69943-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="69943-112">Area:</span></span>  <br/> |<span data-ttu-id="69943-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="69943-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69943-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="69943-114">Remarks</span></span>

<span data-ttu-id="69943-115">À l'aide d'une boîte de dialogue de l'applet du panneau de configuration, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="69943-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="69943-116">Par exemple, l'utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (dll) qui appartiennent au service.</span><span class="sxs-lookup"><span data-stu-id="69943-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="69943-117">L'utilisateur peut ensuite Rechercher des détails supplémentaires sur les fichiers spécifiés, tels que les noms et les numéros de version de toutes les dll.</span><span class="sxs-lookup"><span data-stu-id="69943-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="69943-118">MAPI utilise les propriétés suivantes pour créer une liste de fichiers de prise en charge dans une boîte de dialogue pour la sélection de l'utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="69943-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="69943-119">MAPI fonctionne uniquement avec les noms de fichier et les autres chaînes qui lui sont transmises, dans le jeu de caractères ANSI (Active Directory Service Interfaces).</span><span class="sxs-lookup"><span data-stu-id="69943-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="69943-120">Les applications clientes qui utilisent des noms de fichier dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d'appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="69943-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69943-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="69943-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="69943-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="69943-122">Header files</span></span>

<span data-ttu-id="69943-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="69943-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="69943-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="69943-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="69943-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="69943-125">Mapitags.h</span></span>
  
> <span data-ttu-id="69943-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="69943-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69943-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69943-127">See also</span></span>



[<span data-ttu-id="69943-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="69943-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69943-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="69943-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69943-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="69943-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69943-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="69943-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

