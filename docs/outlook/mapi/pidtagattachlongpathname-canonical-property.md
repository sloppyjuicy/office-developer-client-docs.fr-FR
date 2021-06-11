---
title: Propriété canonique PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339367"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="fcc57-103">Propriété canonique PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="fcc57-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="fcc57-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcc57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcc57-105">Contient le chemin d’accès complet et le nom de fichier complets d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fcc57-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcc57-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fcc57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcc57-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="fcc57-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="fcc57-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fcc57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fcc57-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="fcc57-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="fcc57-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fcc57-110">Data type:</span></span>  <br/> |<span data-ttu-id="fcc57-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fcc57-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fcc57-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fcc57-112">Area:</span></span>  <br/> |<span data-ttu-id="fcc57-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="fcc57-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcc57-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fcc57-114">Remarks</span></span>

<span data-ttu-id="fcc57-115">Ces propriétés sont applicables lorsque vous utilisez l’une des valeurs de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent la pièce jointe par référence : **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** ou **ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="fcc57-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="fcc57-116">Les plateformes qui prendre en charge les noms de fichiers longs doivent définir les propriétés **PR_ATTACH_LONG_PATHNAME** ou associées et les propriétés **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) lors de l’envoi, et doivent d’abord vérifier **PR_ATTACH_LONG_PATHNAME** ou les propriétés associées lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="fcc57-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="fcc57-117">L’application cliente doit définir ces propriétés sur un chemin d’accès long et un nom de fichier suggérés à utiliser si l’ordinateur hôte recevant un message prend en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="fcc57-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="fcc57-118">La définition de ces propriétés indique que les données de pièce jointe ne sont pas incluses dans le message, mais sont disponibles sur un serveur de fichiers commun.</span><span class="sxs-lookup"><span data-stu-id="fcc57-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="fcc57-119">Contrairement aux répertoires et noms de fichiers fournis par **PR_ATTACH_PATHNAME,** ces répertoires et noms de fichiers ne sont pas limités à un répertoire ou un nom de fichier à huit caractères plus une extension à trois caractères.</span><span class="sxs-lookup"><span data-stu-id="fcc57-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="fcc57-120">Au lieu de cela, chaque répertoire ou nom de fichier peut avoir jusqu’à 256 caractères, y compris le nom, l’extension et la période de séparation.</span><span class="sxs-lookup"><span data-stu-id="fcc57-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="fcc57-121">Toutefois, le chemin d’accès global est limité à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="fcc57-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="fcc57-122">Les clients doivent utiliser une convention d’attribution de noms universelle (UNC) dans la plupart des cas lorsque le fichier est partagé et doivent utiliser un chemin d’accès absolu lorsque le fichier est local.</span><span class="sxs-lookup"><span data-stu-id="fcc57-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="fcc57-123">MAPI fonctionne uniquement avec les chemins d’accès et les noms de fichiers dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="fcc57-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="fcc57-124">Les applications clientes qui utilisent des chemins d’accès et des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcc57-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fcc57-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fcc57-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcc57-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="fcc57-126">Protocol specifications</span></span>

<span data-ttu-id="fcc57-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcc57-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcc57-128">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="fcc57-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="fcc57-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcc57-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcc57-130">Spécifie les propriétés des messages codés gérés par des droits.</span><span class="sxs-lookup"><span data-stu-id="fcc57-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcc57-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fcc57-131">Header files</span></span>

<span data-ttu-id="fcc57-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcc57-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcc57-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fcc57-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcc57-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fcc57-134">Mapitags.h</span></span>
  
> <span data-ttu-id="fcc57-135">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="fcc57-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcc57-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcc57-136">See also</span></span>



[<span data-ttu-id="fcc57-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fcc57-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcc57-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fcc57-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcc57-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fcc57-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcc57-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fcc57-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

