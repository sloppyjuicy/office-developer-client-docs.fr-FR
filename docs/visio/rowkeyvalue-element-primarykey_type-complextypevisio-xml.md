---
title: Élément RowKeyValue (PrimaryKey_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Spécifie la valeur d’une clé primaire pour une ligne d’un objet recordset.
ms.openlocfilehash: 3b91997b5fe8184eb89f8c53197a512d809171b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789563"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="87e03-103">Élément RowKeyValue (PrimaryKey_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="87e03-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="87e03-104">Spécifie la valeur d’une clé primaire pour une ligne d’un objet recordset.</span><span class="sxs-lookup"><span data-stu-id="87e03-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87e03-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="87e03-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87e03-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="87e03-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87e03-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="87e03-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87e03-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="87e03-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87e03-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="87e03-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87e03-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87e03-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87e03-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="87e03-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87e03-112">recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="87e03-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87e03-113">Définition</span><span class="sxs-lookup"><span data-stu-id="87e03-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87e03-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="87e03-114">Elements and attributes</span></span>

<span data-ttu-id="87e03-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="87e03-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87e03-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="87e03-116">Parent elements</span></span>

|<span data-ttu-id="87e03-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="87e03-117">**Element**</span></span>|<span data-ttu-id="87e03-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="87e03-118">**Type**</span></span>|<span data-ttu-id="87e03-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="87e03-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87e03-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="87e03-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87e03-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="87e03-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87e03-122">Spécifie une clé primaire d’un objet recordset.</span><span class="sxs-lookup"><span data-stu-id="87e03-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87e03-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="87e03-123">Child elements</span></span>

<span data-ttu-id="87e03-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87e03-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87e03-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="87e03-125">Attributes</span></span>

|<span data-ttu-id="87e03-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="87e03-126">**Attribute**</span></span>|<span data-ttu-id="87e03-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="87e03-127">**Type**</span></span>|<span data-ttu-id="87e03-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="87e03-128">**Required**</span></span>|<span data-ttu-id="87e03-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="87e03-129">**Description**</span></span>|<span data-ttu-id="87e03-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="87e03-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87e03-131">RowID</span><span class="sxs-lookup"><span data-stu-id="87e03-131">RowID</span></span>  <br/> |<span data-ttu-id="87e03-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="87e03-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87e03-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="87e03-133">required</span></span>  <br/> |<span data-ttu-id="87e03-134">Valeur unique qui identifie une ligne d’un objet recordset.</span><span class="sxs-lookup"><span data-stu-id="87e03-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="87e03-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="87e03-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="87e03-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="87e03-136">Value</span></span>  <br/> |<span data-ttu-id="87e03-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="87e03-137">xsd:string</span></span>  <br/> |<span data-ttu-id="87e03-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="87e03-138">required</span></span>  <br/> |<span data-ttu-id="87e03-139">La valeur de la clé primaire de cette ligne de l’objet recordset.</span><span class="sxs-lookup"><span data-stu-id="87e03-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="87e03-140">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="87e03-140">Values of the xsd:string type.</span></span>  <br/> |
   

