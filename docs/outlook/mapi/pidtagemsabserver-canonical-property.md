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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335797"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="d793a-103">Propriété canonique PidTagEmsAbServer</span><span class="sxs-lookup"><span data-stu-id="d793a-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="d793a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d793a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d793a-105">Spécifie le chemin d’accès d’un conteneur de carnet d’adresses dans un scénario hors connexion ou le nom de domaine complet du serveur de catalogue global où réside le conteneur de carnet d’adresses dans un scénario en ligne.</span><span class="sxs-lookup"><span data-stu-id="d793a-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="d793a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d793a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d793a-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="d793a-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="d793a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d793a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d793a-109">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="d793a-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="d793a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d793a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d793a-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="d793a-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="d793a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d793a-112">Area:</span></span>  <br/> |<span data-ttu-id="d793a-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="d793a-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d793a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d793a-114">Remarks</span></span>

<span data-ttu-id="d793a-115">Cette propriété a le type de propriété réinitialisé à **PT_UNICODE** lorsqu’elle est compilée avec le symbole sur une plateforme Unicode et à PT_STRING8 lorsqu’elle n’est pas compilée avec le `UNICODE`  `UNICODE` symbole.</span><span class="sxs-lookup"><span data-stu-id="d793a-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d793a-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d793a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d793a-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d793a-117">Protocol specifications</span></span>

<span data-ttu-id="d793a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d793a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d793a-119">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d793a-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d793a-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d793a-120">Header files</span></span>

<span data-ttu-id="d793a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d793a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d793a-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d793a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d793a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d793a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d793a-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d793a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d793a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d793a-125">See also</span></span>



[<span data-ttu-id="d793a-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d793a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d793a-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d793a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d793a-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d793a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d793a-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d793a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

