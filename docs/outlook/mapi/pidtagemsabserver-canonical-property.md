---
title: Propriété canonique PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384976"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="6f23c-103">Propriété canonique PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="6f23c-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="6f23c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f23c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f23c-105">Spécifie le chemin d’accès d’un conteneur de carnet d’adresses dans un scénario en mode hors connexion ou le nom de domaine complet du serveur de catalogue global où le conteneur de carnet d’adresses se trouve dans un scénario en ligne.</span><span class="sxs-lookup"><span data-stu-id="6f23c-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6f23c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f23c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f23c-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="6f23c-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="6f23c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f23c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f23c-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="6f23c-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="6f23c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f23c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f23c-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="6f23c-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="6f23c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6f23c-112">Area:</span></span>  <br/> |<span data-ttu-id="6f23c-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="6f23c-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f23c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f23c-114">Remarks</span></span>

<span data-ttu-id="6f23c-115">Cette propriété est le type de propriété rétablir **PT_UNICODE** lorsqu’il est compilé avec la `UNICODE` symbole sur une plateforme Unicode et **PT_STRING8** lorsqu’il n’est pas compilé avec la `UNICODE` symbole.</span><span class="sxs-lookup"><span data-stu-id="6f23c-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f23c-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6f23c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f23c-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6f23c-117">Protocol specifications</span></span>

<span data-ttu-id="6f23c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f23c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f23c-119">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f23c-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f23c-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6f23c-120">Header files</span></span>

<span data-ttu-id="6f23c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f23c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f23c-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6f23c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f23c-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6f23c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6f23c-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6f23c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f23c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f23c-125">See also</span></span>



[<span data-ttu-id="6f23c-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f23c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f23c-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6f23c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f23c-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6f23c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f23c-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6f23c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

