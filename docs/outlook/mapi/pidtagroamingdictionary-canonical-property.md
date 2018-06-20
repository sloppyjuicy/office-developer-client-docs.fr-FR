---
title: Propriété canonique PidTagRoamingDictionary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786626"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="da663-103">Propriété canonique PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="da663-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="da663-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da663-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da663-105">Contient un document XML qui décrit le dictionnaire d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="da663-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da663-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="da663-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da663-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="da663-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="da663-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="da663-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da663-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="da663-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="da663-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="da663-110">Data type:</span></span>  <br/> |<span data-ttu-id="da663-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="da663-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="da663-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="da663-112">Area:</span></span>  <br/> |<span data-ttu-id="da663-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="da663-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da663-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="da663-114">Remarks</span></span>

<span data-ttu-id="da663-115">Cette propriété contient un document XML UNICODE qui est en utilisant le codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="da663-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="da663-116">Un message avec un flux de dictionnaire doit définir cette propriété avec le schéma suivant :</span><span class="sxs-lookup"><span data-stu-id="da663-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="da663-117">Vous trouverez ci-dessous un exemple de document XML stockée dans cette propriété sur un message de données de Configuration :</span><span class="sxs-lookup"><span data-stu-id="da663-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="da663-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="da663-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da663-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="da663-119">Protocol specifications</span></span>

<span data-ttu-id="da663-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da663-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da663-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="da663-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da663-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da663-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da663-123">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="da663-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da663-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="da663-124">Header files</span></span>

<span data-ttu-id="da663-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da663-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="da663-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="da663-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="da663-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="da663-127">Mapitags.h</span></span>
  
> <span data-ttu-id="da663-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="da663-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da663-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da663-129">See also</span></span>



[<span data-ttu-id="da663-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="da663-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da663-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="da663-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da663-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="da663-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da663-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="da663-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

