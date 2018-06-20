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
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786782"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="47a38-103">Propriété canonique PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="47a38-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="47a38-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47a38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47a38-105">Contient le nom d’un service de message tel que défini par l’utilisateur dans le fichier MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="47a38-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47a38-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="47a38-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47a38-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="47a38-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="47a38-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="47a38-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47a38-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="47a38-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="47a38-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="47a38-110">Data type:</span></span>  <br/> |<span data-ttu-id="47a38-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47a38-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47a38-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="47a38-112">Area:</span></span>  <br/> |<span data-ttu-id="47a38-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="47a38-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47a38-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="47a38-114">Remarks</span></span>

<span data-ttu-id="47a38-115">Le nom figurant dans ces propriétés est spécifique au service de message.</span><span class="sxs-lookup"><span data-stu-id="47a38-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="47a38-116">Il s’agit de la section [Services] dans MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="47a38-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="47a38-117">Ces propriétés apparaissent sous la forme d’une colonne dans la table de service de message et peuvent être utilisées pour filtrer les services.</span><span class="sxs-lookup"><span data-stu-id="47a38-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="47a38-118">Car elle est utilisée pour identifier et filtrer les services, la valeur ne doit pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="47a38-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47a38-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="47a38-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="47a38-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="47a38-120">Header files</span></span>

<span data-ttu-id="47a38-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47a38-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="47a38-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="47a38-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="47a38-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="47a38-123">Mapitags.h</span></span>
  
> <span data-ttu-id="47a38-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="47a38-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47a38-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a38-125">See also</span></span>



[<span data-ttu-id="47a38-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="47a38-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47a38-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="47a38-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47a38-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="47a38-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47a38-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="47a38-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

