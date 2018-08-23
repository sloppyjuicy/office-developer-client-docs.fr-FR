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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3bf6347102fc0865b081847a0b66763ba2654665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589482"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="4122d-103">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="4122d-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="4122d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4122d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4122d-105">Contient le nom de fichier de base de la bibliothèque de liens dynamiques fournisseur MAPI service (DLL).</span><span class="sxs-lookup"><span data-stu-id="4122d-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4122d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4122d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4122d-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4122d-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4122d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4122d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4122d-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="4122d-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="4122d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4122d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4122d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4122d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4122d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4122d-112">Area:</span></span>  <br/> |<span data-ttu-id="4122d-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="4122d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4122d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4122d-114">Remarks</span></span>

<span data-ttu-id="4122d-115">MAPI utilise une convention d’affectation de noms de fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="4122d-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="4122d-116">Nom de base contient les caractères jusqu'à six identifient de manière unique la DLL.</span><span class="sxs-lookup"><span data-stu-id="4122d-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="4122d-117">MAPI ajoute la chaîne 32 sur le nom DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4122d-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="4122d-118">Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom du fichier MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="4122d-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="4122d-119">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="4122d-119">These properties should specify the base name.</span></span> <span data-ttu-id="4122d-120">MAPI ajoute la chaîne 32 comme il convient.</span><span class="sxs-lookup"><span data-stu-id="4122d-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="4122d-121">Dans le cadre de cette propriété entraîne une erreur, y compris la chaîne 32.</span><span class="sxs-lookup"><span data-stu-id="4122d-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4122d-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4122d-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4122d-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4122d-123">Header files</span></span>

<span data-ttu-id="4122d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4122d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4122d-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4122d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4122d-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4122d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4122d-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4122d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4122d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4122d-128">See also</span></span>



[<span data-ttu-id="4122d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4122d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4122d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4122d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4122d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4122d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4122d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4122d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

