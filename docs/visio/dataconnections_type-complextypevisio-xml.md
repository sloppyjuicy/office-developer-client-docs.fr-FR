---
title: Type complexe DataConnections_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788409"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="48f40-102">Type complexe DataConnections_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="48f40-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="48f40-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="48f40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48f40-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="48f40-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48f40-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="48f40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48f40-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48f40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48f40-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="48f40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48f40-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="48f40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48f40-109">Définition</span><span class="sxs-lookup"><span data-stu-id="48f40-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="48f40-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="48f40-110">Elements and attributes</span></span>

<span data-ttu-id="48f40-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="48f40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48f40-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="48f40-112">Child elements</span></span>

|<span data-ttu-id="48f40-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48f40-113">**Element**</span></span>|<span data-ttu-id="48f40-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="48f40-114">**Type**</span></span>|<span data-ttu-id="48f40-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="48f40-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48f40-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="48f40-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48f40-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="48f40-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="48f40-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="48f40-118">Attributes</span></span>

|<span data-ttu-id="48f40-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48f40-119">**Attribute**</span></span>|<span data-ttu-id="48f40-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="48f40-120">**Type**</span></span>|<span data-ttu-id="48f40-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="48f40-121">**Required**</span></span>|<span data-ttu-id="48f40-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="48f40-122">**Description**</span></span>|<span data-ttu-id="48f40-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="48f40-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48f40-124">NextID</span><span class="sxs-lookup"><span data-stu-id="48f40-124">NextID</span></span>  <br/> |<span data-ttu-id="48f40-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48f40-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48f40-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48f40-126">required</span></span>  <br/> ||<span data-ttu-id="48f40-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="48f40-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

