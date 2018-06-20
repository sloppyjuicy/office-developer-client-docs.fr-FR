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
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786781"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="92a3d-103">Propriété canonique PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="92a3d-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="92a3d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92a3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92a3d-105">Contient le nom de fichier de la DLL contenant la fonction de point d’entrée de message service fournisseur à appeler pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="92a3d-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92a3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="92a3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92a3d-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="92a3d-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="92a3d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="92a3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92a3d-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="92a3d-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="92a3d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="92a3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="92a3d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92a3d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="92a3d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="92a3d-112">Area:</span></span>  <br/> |<span data-ttu-id="92a3d-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="92a3d-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92a3d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="92a3d-114">Remarks</span></span>

<span data-ttu-id="92a3d-115">Lorsque le nom de la fonction point d’entrée apparaît dans la méthode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), il indique que le point d’entrée existe.</span><span class="sxs-lookup"><span data-stu-id="92a3d-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="92a3d-116">MAPI utilise une convention d’affectation de noms de fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="92a3d-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="92a3d-117">Nom de base contient les caractères jusqu'à six identifient de manière unique la DLL.</span><span class="sxs-lookup"><span data-stu-id="92a3d-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="92a3d-118">MAPI ajoute la chaîne 32 sur le nom DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92a3d-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="92a3d-119">Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom du fichier MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.</span><span class="sxs-lookup"><span data-stu-id="92a3d-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="92a3d-120">Ces propriétés doivent spécifier le nom de base.</span><span class="sxs-lookup"><span data-stu-id="92a3d-120">These properties should specify the base name.</span></span> <span data-ttu-id="92a3d-121">MAPI ajoute la chaîne 32 comme il convient.</span><span class="sxs-lookup"><span data-stu-id="92a3d-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="92a3d-122">Dans le cadre du résultat de ces propriétés dans une erreur, y compris la chaîne 32.</span><span class="sxs-lookup"><span data-stu-id="92a3d-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92a3d-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="92a3d-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="92a3d-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="92a3d-124">Header files</span></span>

<span data-ttu-id="92a3d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92a3d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="92a3d-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="92a3d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="92a3d-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="92a3d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="92a3d-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="92a3d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92a3d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a3d-129">See also</span></span>



[<span data-ttu-id="92a3d-130">Propriété canonique PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="92a3d-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="92a3d-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="92a3d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92a3d-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="92a3d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92a3d-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="92a3d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92a3d-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="92a3d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

