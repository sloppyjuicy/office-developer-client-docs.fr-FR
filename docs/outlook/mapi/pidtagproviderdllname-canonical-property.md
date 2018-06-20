---
title: Propriété canonique PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786457"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="add93-103">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="add93-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="add93-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="add93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="add93-105">Contient le nom de fichier de base de la bibliothèque de liens dynamiques fournisseur MAPI service (DLL).</span><span class="sxs-lookup"><span data-stu-id="add93-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="add93-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="add93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="add93-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="add93-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="add93-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="add93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="add93-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="add93-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="add93-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="add93-110">Data type:</span></span>  <br/> |<span data-ttu-id="add93-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="add93-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="add93-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="add93-112">Area:</span></span>  <br/> |<span data-ttu-id="add93-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="add93-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="add93-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="add93-114">Remarks</span></span>

<span data-ttu-id="add93-115">MAPI utilise une convention d’affectation de noms de fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="add93-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="add93-116">Nom de base contient les caractères jusqu'à six identifient de manière unique la DLL.</span><span class="sxs-lookup"><span data-stu-id="add93-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="add93-117">MAPI ajoute la chaîne 32 sur le nom DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="add93-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="add93-118">Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom du fichier MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="add93-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="add93-119">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="add93-119">These properties should specify the base name.</span></span> <span data-ttu-id="add93-120">MAPI ajoute la chaîne 32 comme il convient.</span><span class="sxs-lookup"><span data-stu-id="add93-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="add93-121">Dans le cadre de cette propriété entraîne une erreur, y compris la chaîne 32.</span><span class="sxs-lookup"><span data-stu-id="add93-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="add93-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="add93-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="add93-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="add93-123">Header files</span></span>

<span data-ttu-id="add93-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="add93-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="add93-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="add93-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="add93-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="add93-126">Mapitags.h</span></span>
  
> <span data-ttu-id="add93-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="add93-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="add93-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="add93-128">See also</span></span>



[<span data-ttu-id="add93-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="add93-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="add93-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="add93-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="add93-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="add93-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="add93-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="add93-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

