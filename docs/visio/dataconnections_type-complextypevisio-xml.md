---
title: DataConnections_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542456"
---
# <a name="dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="f4883-102">DataConnections_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f4883-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f4883-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f4883-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4883-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4883-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f4883-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f4883-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f4883-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f4883-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f4883-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f4883-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f4883-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f4883-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4883-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f4883-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f4883-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f4883-110">Elements and attributes</span></span>

<span data-ttu-id="f4883-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="f4883-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f4883-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f4883-112">Child elements</span></span>

|<span data-ttu-id="f4883-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f4883-113">**Element**</span></span>|<span data-ttu-id="f4883-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f4883-114">**Type**</span></span>|<span data-ttu-id="f4883-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4883-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4883-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="f4883-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4883-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="f4883-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f4883-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="f4883-118">Attributes</span></span>

|<span data-ttu-id="f4883-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f4883-119">**Attribute**</span></span>|<span data-ttu-id="f4883-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="f4883-120">**Type**</span></span>|<span data-ttu-id="f4883-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f4883-121">**Required**</span></span>|<span data-ttu-id="f4883-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4883-122">**Description**</span></span>|<span data-ttu-id="f4883-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f4883-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4883-124">NextID</span><span class="sxs-lookup"><span data-stu-id="f4883-124">NextID</span></span>  <br/> |<span data-ttu-id="f4883-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f4883-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f4883-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f4883-126">required</span></span>  <br/> ||<span data-ttu-id="f4883-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f4883-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

