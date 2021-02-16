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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4b2aa12b1b81dfd218781a839f5f84881763ef06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359548"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="59e11-103">Propriété canonique PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="59e11-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="59e11-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59e11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59e11-105">Contient un document XML qui décrit le dictionnaire itinérant.</span><span class="sxs-lookup"><span data-stu-id="59e11-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59e11-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="59e11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59e11-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="59e11-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="59e11-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="59e11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59e11-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="59e11-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="59e11-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="59e11-110">Data type:</span></span>  <br/> |<span data-ttu-id="59e11-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="59e11-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="59e11-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="59e11-112">Area:</span></span>  <br/> |<span data-ttu-id="59e11-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="59e11-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e11-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="59e11-114">Remarks</span></span>

<span data-ttu-id="59e11-115">Cette propriété contient un document XML UNICODE qui utilise le codage UTF8.</span><span class="sxs-lookup"><span data-stu-id="59e11-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="59e11-116">Un message avec un flux de dictionnaire doit définir cette propriété avec le schéma suivant :</span><span class="sxs-lookup"><span data-stu-id="59e11-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="https://www.w3.org/2001/XMLSchema"> 
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

<span data-ttu-id="59e11-117">Voici un exemple de document XML stocké dans cette propriété dans un message de données de configuration :</span><span class="sxs-lookup"><span data-stu-id="59e11-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
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

## <a name="related-resources"></a><span data-ttu-id="59e11-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="59e11-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59e11-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="59e11-119">Protocol specifications</span></span>

<span data-ttu-id="59e11-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59e11-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59e11-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="59e11-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59e11-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59e11-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59e11-123">Spécifie l’emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="59e11-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59e11-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="59e11-124">Header files</span></span>

<span data-ttu-id="59e11-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59e11-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="59e11-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="59e11-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="59e11-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59e11-127">Mapitags.h</span></span>
  
> <span data-ttu-id="59e11-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="59e11-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59e11-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59e11-129">See also</span></span>



[<span data-ttu-id="59e11-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="59e11-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59e11-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="59e11-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59e11-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="59e11-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59e11-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="59e11-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

