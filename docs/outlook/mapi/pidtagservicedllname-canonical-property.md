---
title: Propriété canonique PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980453"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="4c533-103">Propriété canonique PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="4c533-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="4c533-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c533-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c533-105">Contient le nom de fichier de la DLL contenant la fonction de point d'entrée du fournisseur de services de messagerie à appeler pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="4c533-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c533-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4c533-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c533-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4c533-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4c533-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4c533-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c533-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="4c533-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="4c533-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4c533-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c533-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4c533-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4c533-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4c533-112">Area:</span></span>  <br/> |<span data-ttu-id="4c533-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="4c533-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c533-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c533-114">Remarks</span></span>

<span data-ttu-id="4c533-115">Lorsque le nom de la fonction de point d'entrée apparaît dans la méthode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), cela indique que le point d'entrée existe.</span><span class="sxs-lookup"><span data-stu-id="4c533-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="4c533-116">MAPI utilise une convention d'affectation de noms de fichiers DLL.</span><span class="sxs-lookup"><span data-stu-id="4c533-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="4c533-117">Il ajoute la chaîne 32 au nom de la DLL de base pour identifier la version qui s'exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4c533-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="4c533-118">Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="4c533-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="4c533-119">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="4c533-119">These properties should specify the base name.</span></span> <span data-ttu-id="4c533-120">MAPI ajoute la chaîne 32 comme il convient.</span><span class="sxs-lookup"><span data-stu-id="4c533-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="4c533-121">L'inclusion de la chaîne 32 dans le cadre de ces propriétés génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="4c533-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c533-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="4c533-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c533-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="4c533-123">Header files</span></span>

<span data-ttu-id="4c533-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4c533-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c533-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4c533-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c533-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4c533-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4c533-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="4c533-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c533-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c533-128">See also</span></span>



[<span data-ttu-id="4c533-129">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="4c533-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="4c533-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4c533-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c533-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4c533-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c533-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4c533-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c533-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4c533-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

