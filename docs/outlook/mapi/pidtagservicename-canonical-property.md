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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438959"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="9b24b-103">Propriété canonique PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="9b24b-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="9b24b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b24b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b24b-105">Contient le nom d’un service de message tel que définie par l’utilisateur dans le fichier MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9b24b-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b24b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9b24b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b24b-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9b24b-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9b24b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9b24b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b24b-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="9b24b-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="9b24b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9b24b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b24b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b24b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b24b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9b24b-112">Area:</span></span>  <br/> |<span data-ttu-id="9b24b-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="9b24b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b24b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b24b-114">Remarks</span></span>

<span data-ttu-id="9b24b-115">Le nom contenu dans ces propriétés est spécifique au service de message.</span><span class="sxs-lookup"><span data-stu-id="9b24b-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="9b24b-116">Il provient de la section [Services] dans MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9b24b-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="9b24b-117">Ces propriétés apparaissent en tant que colonnes dans la table des services de message et peuvent être utilisées pour filtrer les services.</span><span class="sxs-lookup"><span data-stu-id="9b24b-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="9b24b-118">Étant donné qu’elle est utilisée pour identifier et filtrer les services, la valeur ne doit pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="9b24b-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b24b-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9b24b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9b24b-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9b24b-120">Header files</span></span>

<span data-ttu-id="9b24b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b24b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b24b-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9b24b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b24b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9b24b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="9b24b-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9b24b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b24b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b24b-125">See also</span></span>



[<span data-ttu-id="9b24b-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9b24b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b24b-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9b24b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b24b-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9b24b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b24b-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9b24b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

