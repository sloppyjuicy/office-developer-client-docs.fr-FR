---
title: Propriété canonique PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786773"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="6d438-103">Propriété canonique PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="6d438-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="6d438-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d438-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d438-105">Contient le nom de la fonction de point d’entrée pour la configuration d’un service de message.</span><span class="sxs-lookup"><span data-stu-id="6d438-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d438-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6d438-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d438-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="6d438-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="6d438-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6d438-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d438-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="6d438-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="6d438-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6d438-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d438-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6d438-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6d438-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6d438-112">Area:</span></span>  <br/> |<span data-ttu-id="6d438-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="6d438-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d438-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d438-114">Remarks</span></span>

<span data-ttu-id="6d438-115">Il est recommandé que l’implémentation de service de message fournit un point d’entrée de service message, mais le point d’entrée n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6d438-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="6d438-116">Toutefois, le point d’entrée doit être fourni uniquement si les propriétés de configuration associées existent.</span><span class="sxs-lookup"><span data-stu-id="6d438-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="6d438-117">Si ces propriétés n’existent pas, MAPI suppose qu’aucun point d’entrée n’est fournie.</span><span class="sxs-lookup"><span data-stu-id="6d438-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="6d438-118">La bibliothèque de liens dynamiques (DLL) dans lequel la fonction de point d’entrée apparaît est nommée par la propriété **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6d438-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6d438-119">Pour plus d’informations sur les points d’entrée de service de message, voir [mise en œuvre de la fonction de Point d’entrée un fournisseur de Service](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="6d438-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d438-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6d438-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d438-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6d438-121">Header files</span></span>

<span data-ttu-id="6d438-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d438-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d438-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6d438-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d438-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6d438-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6d438-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6d438-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d438-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d438-126">See also</span></span>



[<span data-ttu-id="6d438-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6d438-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d438-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6d438-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d438-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6d438-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d438-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6d438-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

