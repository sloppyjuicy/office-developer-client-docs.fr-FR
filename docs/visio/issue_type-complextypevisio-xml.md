---
title: Type complexe Issue_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399696"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="43b41-102">Type complexe Issue_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="43b41-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43b41-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="43b41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43b41-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="43b41-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43b41-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="43b41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43b41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="43b41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43b41-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="43b41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43b41-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="43b41-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43b41-109">Définition</span><span class="sxs-lookup"><span data-stu-id="43b41-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43b41-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="43b41-110">Elements and attributes</span></span>

<span data-ttu-id="43b41-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="43b41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43b41-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43b41-112">Child elements</span></span>

|<span data-ttu-id="43b41-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="43b41-113">**Element**</span></span>|<span data-ttu-id="43b41-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="43b41-114">**Type**</span></span>|<span data-ttu-id="43b41-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="43b41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43b41-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="43b41-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43b41-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="43b41-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="43b41-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="43b41-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43b41-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="43b41-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="43b41-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="43b41-120">Attributes</span></span>

|<span data-ttu-id="43b41-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="43b41-121">**Attribute**</span></span>|<span data-ttu-id="43b41-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="43b41-122">**Type**</span></span>|<span data-ttu-id="43b41-123">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="43b41-123">**Required**</span></span>|<span data-ttu-id="43b41-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="43b41-124">**Description**</span></span>|<span data-ttu-id="43b41-125">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="43b41-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43b41-126">ID</span><span class="sxs-lookup"><span data-stu-id="43b41-126">ID</span></span>  <br/> |<span data-ttu-id="43b41-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="43b41-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="43b41-128">obligatoire</span><span class="sxs-lookup"><span data-stu-id="43b41-128">required</span></span>  <br/> ||<span data-ttu-id="43b41-129">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="43b41-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="43b41-130">Ignoré</span><span class="sxs-lookup"><span data-stu-id="43b41-130">Ignored</span></span>  <br/> |<span data-ttu-id="43b41-131">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="43b41-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="43b41-132">facultatif</span><span class="sxs-lookup"><span data-stu-id="43b41-132">optional</span></span>  <br/> ||<span data-ttu-id="43b41-133">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="43b41-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

