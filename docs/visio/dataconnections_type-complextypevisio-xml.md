---
title: ComplexType DataConnections_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 2bbea48e1d5340c5a68bbafbef9a900a98357385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360374"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="ec77d-102">ComplexType DataConnections_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ec77d-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec77d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ec77d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec77d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ec77d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec77d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ec77d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec77d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ec77d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec77d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ec77d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec77d-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="ec77d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec77d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ec77d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec77d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ec77d-110">Elements and attributes</span></span>

<span data-ttu-id="ec77d-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ec77d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec77d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ec77d-112">Child elements</span></span>

|<span data-ttu-id="ec77d-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ec77d-113">**Element**</span></span>|<span data-ttu-id="ec77d-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ec77d-114">**Type**</span></span>|<span data-ttu-id="ec77d-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec77d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec77d-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="ec77d-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec77d-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="ec77d-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec77d-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ec77d-118">Attributes</span></span>

|<span data-ttu-id="ec77d-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ec77d-119">**Attribute**</span></span>|<span data-ttu-id="ec77d-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="ec77d-120">**Type**</span></span>|<span data-ttu-id="ec77d-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ec77d-121">**Required**</span></span>|<span data-ttu-id="ec77d-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec77d-122">**Description**</span></span>|<span data-ttu-id="ec77d-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ec77d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec77d-124">NextID</span><span class="sxs-lookup"><span data-stu-id="ec77d-124">NextID</span></span>  <br/> |<span data-ttu-id="ec77d-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec77d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec77d-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ec77d-126">required</span></span>  <br/> ||<span data-ttu-id="ec77d-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec77d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

