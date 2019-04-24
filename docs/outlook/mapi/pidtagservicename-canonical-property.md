---
title: Propriété canonique PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359478"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="e48b6-103">Propriété canonique PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="e48b6-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="e48b6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e48b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e48b6-105">Contient le nom d'un service de messagerie tel que défini par l'utilisateur dans le fichier MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="e48b6-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e48b6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e48b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e48b6-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e48b6-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e48b6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e48b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e48b6-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="e48b6-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="e48b6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e48b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="e48b6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e48b6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e48b6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e48b6-112">Area:</span></span>  <br/> |<span data-ttu-id="e48b6-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="e48b6-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e48b6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e48b6-114">Remarks</span></span>

<span data-ttu-id="e48b6-115">Le nom contenu dans ces propriétés est propre au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e48b6-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="e48b6-116">Elle provient de la section [services] du fichier MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="e48b6-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="e48b6-117">Ces propriétés apparaissent sous la forme d'une colonne dans le tableau service de messagerie et peuvent être utilisées pour filtrer les services.</span><span class="sxs-lookup"><span data-stu-id="e48b6-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="e48b6-118">Étant donné qu'il est utilisé pour identifier et filtrer des services, la valeur ne doit pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="e48b6-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e48b6-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e48b6-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e48b6-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e48b6-120">Header files</span></span>

<span data-ttu-id="e48b6-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e48b6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e48b6-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e48b6-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e48b6-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e48b6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e48b6-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="e48b6-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e48b6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e48b6-125">See also</span></span>



[<span data-ttu-id="e48b6-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e48b6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e48b6-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e48b6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e48b6-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e48b6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e48b6-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e48b6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

