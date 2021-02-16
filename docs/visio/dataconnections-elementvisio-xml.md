---
title: Élément DataConnections (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contient les éléments DataConnection du document.
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539181"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="aa084-103">Élément DataConnections (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aa084-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="aa084-104">Contient les **éléments DataConnection** du document.</span><span class="sxs-lookup"><span data-stu-id="aa084-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="aa084-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="aa084-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa084-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="aa084-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aa084-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="aa084-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aa084-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aa084-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aa084-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="aa084-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aa084-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aa084-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aa084-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="aa084-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aa084-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="aa084-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa084-113">Définition</span><span class="sxs-lookup"><span data-stu-id="aa084-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aa084-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="aa084-114">Elements and attributes</span></span>

<span data-ttu-id="aa084-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="aa084-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aa084-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aa084-116">Parent elements</span></span>

<span data-ttu-id="aa084-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="aa084-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa084-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aa084-118">Child elements</span></span>

|<span data-ttu-id="aa084-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="aa084-119">**Element**</span></span>|<span data-ttu-id="aa084-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="aa084-120">**Type**</span></span>|<span data-ttu-id="aa084-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="aa084-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa084-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="aa084-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa084-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="aa084-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aa084-124">Extrait la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.</span><span class="sxs-lookup"><span data-stu-id="aa084-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aa084-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="aa084-125">Attributes</span></span>

|<span data-ttu-id="aa084-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aa084-126">**Attribute**</span></span>|<span data-ttu-id="aa084-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="aa084-127">**Type**</span></span>|<span data-ttu-id="aa084-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="aa084-128">**Required**</span></span>|<span data-ttu-id="aa084-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="aa084-129">**Description**</span></span>|<span data-ttu-id="aa084-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="aa084-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa084-131">NextID</span><span class="sxs-lookup"><span data-stu-id="aa084-131">NextID</span></span>  <br/> |<span data-ttu-id="aa084-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aa084-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aa084-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa084-133">required</span></span>  <br/> |<span data-ttu-id="aa084-134">L’ID disponible suivant pour les nouvelles connexions.</span><span class="sxs-lookup"><span data-stu-id="aa084-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="aa084-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aa084-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

