---
title: Élément PrimaryKey (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifie une ou plusieurs colonnes de clé primaire dans le recordset de données.
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537709"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="5ee6a-103">Élément PrimaryKey (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5ee6a-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5ee6a-104">Identifie une ou plusieurs colonnes de clé primaire dans le recordset de données.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ee6a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="5ee6a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ee6a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5ee6a-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="5ee6a-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5ee6a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5ee6a-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5ee6a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5ee6a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5ee6a-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5ee6a-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="5ee6a-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ee6a-113">Définition</span><span class="sxs-lookup"><span data-stu-id="5ee6a-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5ee6a-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5ee6a-114">Elements and attributes</span></span>

<span data-ttu-id="5ee6a-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5ee6a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5ee6a-116">Parent elements</span></span>

|<span data-ttu-id="5ee6a-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-117">**Element**</span></span>|<span data-ttu-id="5ee6a-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-118">**Type**</span></span>|<span data-ttu-id="5ee6a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ee6a-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="5ee6a-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5ee6a-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="5ee6a-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ee6a-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ee6a-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5ee6a-123">Child elements</span></span>

|<span data-ttu-id="5ee6a-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-124">**Element**</span></span>|<span data-ttu-id="5ee6a-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-125">**Type**</span></span>|<span data-ttu-id="5ee6a-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ee6a-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="5ee6a-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5ee6a-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="5ee6a-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ee6a-129">Spécifie la valeur de ce composant de la clé primaire pour une ligne individuelle d’un recordset.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="5ee6a-130">Il DOIT y avoir au moins une occurrence de cet élément enfant.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5ee6a-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="5ee6a-131">Attributes</span></span>

|<span data-ttu-id="5ee6a-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-132">**Attribute**</span></span>|<span data-ttu-id="5ee6a-133">**Type**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-133">**Type**</span></span>|<span data-ttu-id="5ee6a-134">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-134">**Required**</span></span>|<span data-ttu-id="5ee6a-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-135">**Description**</span></span>|<span data-ttu-id="5ee6a-136">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="5ee6a-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5ee6a-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="5ee6a-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="5ee6a-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ee6a-138">xsd:string</span></span>  <br/> |<span data-ttu-id="5ee6a-139">facultatif</span><span class="sxs-lookup"><span data-stu-id="5ee6a-139">optional</span></span>  <br/> |<span data-ttu-id="5ee6a-140">Spécifie le nom d’un champ qui est un composant de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="5ee6a-141">Il DOIT s’agit de la valeur de l’attribut **ColumnNameID** d’un DataColumn_Type descendant du DataRecordSet_Type dont la clé primaire est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="5ee6a-142">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5ee6a-142">Values of the xsd:string type.</span></span>  <br/> |
   

