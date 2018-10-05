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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383106"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="9975b-103">Propriété canonique PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="9975b-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="9975b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9975b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9975b-105">Contient le long de chemin d’accès complet et le nom d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9975b-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9975b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9975b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9975b-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="9975b-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="9975b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9975b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9975b-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="9975b-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="9975b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9975b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9975b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9975b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9975b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9975b-112">Area:</span></span>  <br/> |<span data-ttu-id="9975b-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="9975b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9975b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9975b-114">Remarks</span></span>

<span data-ttu-id="9975b-115">Ces propriétés sont applicables lorsque vous utilisez une des valeurs de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent les pièces jointes par référence : **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="9975b-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="9975b-116">Plateformes qui prennent en charge les noms de fichiers longs doivent définir les propriétés de **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) lors de l’envoi et doit vérifier \*\*PR_ATTACH_LONG_PATHNAME et de propriétés associées ou les **PR_ATTACH_LONG_PATHNAME** \*\*ou des propriétés associées tout d’abord lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="9975b-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="9975b-117">L’application cliente doit définir ces propriétés pour un chemin d’accès long suggérée et un nom à utiliser si l’ordinateur hôte reçoit un message prend en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="9975b-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="9975b-118">Définition de ces propriétés indique que les données de pièce jointe n’est pas incluses dans le message, mais ne sont disponibles sur un serveur de fichiers communs.</span><span class="sxs-lookup"><span data-stu-id="9975b-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="9975b-119">Contrairement aux répertoires et noms de fichiers fournis par **PR_ATTACH_PATHNAME**, ces répertoires et les noms de fichiers ne sont pas restreints vers un répertoire de huit caractères ou de nom de fichier plus extension de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="9975b-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="9975b-120">Au lieu de cela, chaque répertoire ou un nom de fichier peut être jusqu'à 256 caractères long, y compris le nom, extension et une période séparateur.</span><span class="sxs-lookup"><span data-stu-id="9975b-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="9975b-121">Toutefois, le chemin d’accès globale est limité à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="9975b-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="9975b-122">Clients doivent utiliser une convention de dénomination universelle (UNC) dans la plupart des cas, lorsque le fichier est partagé et doit utiliser un chemin absolu lorsque le fichier est local.</span><span class="sxs-lookup"><span data-stu-id="9975b-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="9975b-123">MAPI ne fonctionne qu’avec les chemins d’accès et le jeu de caractères ANSI, les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9975b-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="9975b-124">Les applications clientes qui utilisent des chemins d’accès et les noms de fichiers dans un jeu de caractères OEM doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9975b-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9975b-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9975b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9975b-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9975b-126">Protocol specifications</span></span>

<span data-ttu-id="9975b-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9975b-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9975b-128">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9975b-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9975b-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9975b-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9975b-130">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="9975b-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9975b-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9975b-131">Header files</span></span>

<span data-ttu-id="9975b-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9975b-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="9975b-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9975b-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="9975b-134">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9975b-134">Mapitags.h</span></span>
  
> <span data-ttu-id="9975b-135">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9975b-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9975b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9975b-136">See also</span></span>



[<span data-ttu-id="9975b-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9975b-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9975b-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9975b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9975b-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9975b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9975b-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9975b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

