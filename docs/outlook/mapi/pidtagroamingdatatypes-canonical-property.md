---
title: Propriété canonique PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d8b4df2dbb0d7fd2edeb82222f333c11c5f71987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786613"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="13ef7-103">Propriété canonique PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="13ef7-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="13ef7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13ef7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13ef7-105">Contient un masque de bits indiquant le flux de propriétés existent sur le message.</span><span class="sxs-lookup"><span data-stu-id="13ef7-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13ef7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="13ef7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13ef7-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="13ef7-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="13ef7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="13ef7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13ef7-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="13ef7-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="13ef7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="13ef7-110">Data type:</span></span>  <br/> |<span data-ttu-id="13ef7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13ef7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13ef7-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="13ef7-112">Area:</span></span>  <br/> |<span data-ttu-id="13ef7-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="13ef7-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13ef7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="13ef7-114">Remarks</span></span>

<span data-ttu-id="13ef7-115">Cette propriété doit être définie à une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="13ef7-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="13ef7-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="13ef7-116">**Value**</span></span>|<span data-ttu-id="13ef7-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="13ef7-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13ef7-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="13ef7-118">0x00000002</span></span>  <br/> |<span data-ttu-id="13ef7-119">Indique que le message du dossier associé informations (FAI) doit contenir un flux de dictionnaire, sérialisées dans un schéma XML fixe et stockées dans la propriété **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="13ef7-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="13ef7-120">Si le message FAI ne contient pas un flux de dictionnaire, l’application doit traiter le dictionnaire qu’aucune entrée.</span><span class="sxs-lookup"><span data-stu-id="13ef7-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="13ef7-121">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="13ef7-121">0x00000004</span></span>  <br/> |<span data-ttu-id="13ef7-122">Indique que le message FAI doit contenir un flux de données XML stockée dans la propriété **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) qui utilise un schéma XML arbitraire.</span><span class="sxs-lookup"><span data-stu-id="13ef7-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="13ef7-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="13ef7-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13ef7-124">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="13ef7-124">Protocol specifications</span></span>

<span data-ttu-id="13ef7-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ef7-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ef7-126">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="13ef7-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13ef7-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ef7-127">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ef7-128">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="13ef7-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13ef7-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="13ef7-129">Header files</span></span>

<span data-ttu-id="13ef7-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13ef7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="13ef7-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="13ef7-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="13ef7-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="13ef7-132">Mapitags.h</span></span>
  
> <span data-ttu-id="13ef7-133">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="13ef7-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13ef7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13ef7-134">See also</span></span>



[<span data-ttu-id="13ef7-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="13ef7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13ef7-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="13ef7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13ef7-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="13ef7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13ef7-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="13ef7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

