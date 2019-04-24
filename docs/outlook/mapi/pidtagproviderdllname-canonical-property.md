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
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286487"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="479d0-103">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="479d0-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="479d0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="479d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="479d0-105">Contient le nom de fichier de base de la bibliothèque de liens dynamiques (DLL) du fournisseur de services MAPI.</span><span class="sxs-lookup"><span data-stu-id="479d0-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="479d0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="479d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="479d0-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="479d0-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="479d0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="479d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="479d0-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="479d0-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="479d0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="479d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="479d0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="479d0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="479d0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="479d0-112">Area:</span></span>  <br/> |<span data-ttu-id="479d0-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="479d0-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="479d0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="479d0-114">Remarks</span></span>

<span data-ttu-id="479d0-115">MAPI utilise une convention d'affectation de noms de fichiers DLL.</span><span class="sxs-lookup"><span data-stu-id="479d0-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="479d0-116">Il ajoute la chaîne 32 au nom de la DLL de base pour identifier la version qui s'exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="479d0-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="479d0-117">Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="479d0-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="479d0-118">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="479d0-118">These properties should specify the base name.</span></span> <span data-ttu-id="479d0-119">MAPI ajoute la chaîne 32 comme il convient.</span><span class="sxs-lookup"><span data-stu-id="479d0-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="479d0-120">L'inclusion de la chaîne 32 dans cette propriété génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="479d0-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="479d0-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="479d0-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="479d0-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="479d0-122">Header files</span></span>

<span data-ttu-id="479d0-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="479d0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="479d0-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="479d0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="479d0-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="479d0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="479d0-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="479d0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="479d0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="479d0-127">See also</span></span>



[<span data-ttu-id="479d0-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="479d0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="479d0-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="479d0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="479d0-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="479d0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="479d0-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="479d0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

