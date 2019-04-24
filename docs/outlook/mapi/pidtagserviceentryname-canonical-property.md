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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351071"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="9bb97-103">Propriété canonique PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="9bb97-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="9bb97-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bb97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bb97-105">Contient le nom de la fonction de point d'entrée pour la configuration d'un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9bb97-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bb97-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9bb97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bb97-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="9bb97-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="9bb97-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9bb97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bb97-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="9bb97-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="9bb97-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9bb97-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bb97-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9bb97-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9bb97-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9bb97-112">Area:</span></span>  <br/> |<span data-ttu-id="9bb97-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb97-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bb97-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bb97-114">Remarks</span></span>

<span data-ttu-id="9bb97-115">Il est recommandé que les implémenteurs de service de message fournissent un point d'entrée de service de messagerie, mais que le point d'entrée ne soit pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9bb97-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="9bb97-116">Toutefois, le point d'entrée doit être fourni uniquement si les propriétés de configuration associées existent.</span><span class="sxs-lookup"><span data-stu-id="9bb97-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="9bb97-117">Si ces propriétés n'existent pas, MAPI suppose qu'aucun point d'entrée n'est fourni.</span><span class="sxs-lookup"><span data-stu-id="9bb97-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="9bb97-118">La bibliothèque de liens dynamiques (DLL) dans laquelle la fonction de point d'entrée apparaît est nommée par la propriété **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9bb97-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9bb97-119">Pour plus d'informations sur les points d'entrée du service de message, voir [implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="9bb97-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bb97-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9bb97-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9bb97-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9bb97-121">Header files</span></span>

<span data-ttu-id="9bb97-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9bb97-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bb97-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9bb97-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bb97-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9bb97-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9bb97-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9bb97-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bb97-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bb97-126">See also</span></span>



[<span data-ttu-id="9bb97-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb97-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bb97-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb97-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bb97-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb97-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bb97-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9bb97-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

