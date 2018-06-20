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
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786814"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="b75fa-103">Propriété canonique PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="b75fa-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="b75fa-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b75fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b75fa-105">Contient une liste des fichiers qui appartiennent au service de message.</span><span class="sxs-lookup"><span data-stu-id="b75fa-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b75fa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b75fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b75fa-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="b75fa-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="b75fa-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b75fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b75fa-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="b75fa-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="b75fa-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b75fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="b75fa-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b75fa-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b75fa-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="b75fa-112">Area:</span></span>  <br/> |<span data-ttu-id="b75fa-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="b75fa-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b75fa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b75fa-114">Remarks</span></span>

<span data-ttu-id="b75fa-115">À l’aide d’une boîte de dialogue dans le panneau, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de message.</span><span class="sxs-lookup"><span data-stu-id="b75fa-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="b75fa-116">Par exemple, l’utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (DLL) qui appartiennent au service.</span><span class="sxs-lookup"><span data-stu-id="b75fa-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="b75fa-117">L’utilisateur peut rechercher puis plus d’informations sur les fichiers spécifiés, tels que les noms et les numéros de version de toutes les DLL.</span><span class="sxs-lookup"><span data-stu-id="b75fa-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="b75fa-118">MAPI utilise ces propriétés pour créer une liste de fichiers de prise en charge dans une boîte de dialogue de sélection de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b75fa-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="b75fa-119">MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères Active Directory Service Interfaces (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b75fa-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="b75fa-120">Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b75fa-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b75fa-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b75fa-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b75fa-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b75fa-122">Header files</span></span>

<span data-ttu-id="b75fa-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b75fa-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b75fa-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b75fa-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b75fa-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b75fa-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b75fa-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b75fa-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b75fa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75fa-127">See also</span></span>



[<span data-ttu-id="b75fa-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b75fa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b75fa-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b75fa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b75fa-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b75fa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b75fa-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b75fa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

