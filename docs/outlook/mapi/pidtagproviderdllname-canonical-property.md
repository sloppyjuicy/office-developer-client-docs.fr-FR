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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286487"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="3be21-103">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="3be21-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="3be21-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3be21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3be21-105">Contient le nom de fichier de base de la bibliothèque de liens dynamiques (DLL) du fournisseur de services MAPI.</span><span class="sxs-lookup"><span data-stu-id="3be21-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3be21-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3be21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3be21-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3be21-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3be21-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3be21-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3be21-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="3be21-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="3be21-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3be21-110">Data type:</span></span>  <br/> |<span data-ttu-id="3be21-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3be21-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3be21-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3be21-112">Area:</span></span>  <br/> |<span data-ttu-id="3be21-113">MAPI courant</span><span class="sxs-lookup"><span data-stu-id="3be21-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3be21-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3be21-114">Remarks</span></span>

<span data-ttu-id="3be21-115">MAPI utilise une convention d’attribution de noms de fichiers DLL.</span><span class="sxs-lookup"><span data-stu-id="3be21-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="3be21-116">Il a ajouté la chaîne 32 au nom de la DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3be21-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="3be21-117">Par exemple, lorsque le nom MAPI.DLL est spécifié, MAPI construit le nom MAPI32.DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="3be21-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="3be21-118">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="3be21-118">These properties should specify the base name.</span></span> <span data-ttu-id="3be21-119">MAPI a ajouté la chaîne 32 selon le cas.</span><span class="sxs-lookup"><span data-stu-id="3be21-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="3be21-120">L’utilisation de la chaîne 32 dans le cadre de cette propriété entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="3be21-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3be21-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3be21-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3be21-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3be21-122">Header files</span></span>

<span data-ttu-id="3be21-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3be21-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3be21-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3be21-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3be21-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3be21-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3be21-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="3be21-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3be21-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3be21-127">See also</span></span>



[<span data-ttu-id="3be21-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3be21-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3be21-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3be21-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3be21-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3be21-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3be21-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3be21-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

