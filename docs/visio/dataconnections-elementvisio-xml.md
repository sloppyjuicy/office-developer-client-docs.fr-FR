---
title: Élément DataConnections (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contient les éléments DataConnection pour le document.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395027"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="b2cc2-103">Élément DataConnections (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b2cc2-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="b2cc2-104">Contient les éléments **DataConnection** pour le document.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b2cc2-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="b2cc2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2cc2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b2cc2-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="b2cc2-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b2cc2-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b2cc2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b2cc2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b2cc2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b2cc2-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b2cc2-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="b2cc2-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2cc2-113">Définition</span><span class="sxs-lookup"><span data-stu-id="b2cc2-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2cc2-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b2cc2-114">Elements and attributes</span></span>

<span data-ttu-id="b2cc2-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b2cc2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b2cc2-116">Parent elements</span></span>

<span data-ttu-id="b2cc2-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2cc2-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b2cc2-118">Child elements</span></span>

|<span data-ttu-id="b2cc2-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-119">**Element**</span></span>|<span data-ttu-id="b2cc2-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-120">**Type**</span></span>|<span data-ttu-id="b2cc2-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2cc2-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="b2cc2-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cc2-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="b2cc2-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2cc2-124">Analyse la communication entre un ou plusieurs éléments **DataRecordset** et une source de données non XML.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b2cc2-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="b2cc2-125">Attributes</span></span>

|<span data-ttu-id="b2cc2-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-126">**Attribute**</span></span>|<span data-ttu-id="b2cc2-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-127">**Type**</span></span>|<span data-ttu-id="b2cc2-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-128">**Required**</span></span>|<span data-ttu-id="b2cc2-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-129">**Description**</span></span>|<span data-ttu-id="b2cc2-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2cc2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2cc2-131">NextID</span><span class="sxs-lookup"><span data-stu-id="b2cc2-131">NextID</span></span>  <br/> |<span data-ttu-id="b2cc2-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2cc2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2cc2-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2cc2-133">required</span></span>  <br/> |<span data-ttu-id="b2cc2-134">L’ID suivant disponible pour les nouvelles connexions.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="b2cc2-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2cc2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

