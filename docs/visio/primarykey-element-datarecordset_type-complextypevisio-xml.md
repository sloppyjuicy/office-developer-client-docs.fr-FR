---
title: PrimaryKey, élément (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifie une ou plusieurs colonnes de clé primaire du jeu d’enregistrements de données.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396357"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="1c691-103">PrimaryKey, élément (DataRecordSet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1c691-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1c691-104">Identifie une ou plusieurs colonnes de clé primaire du jeu d’enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="1c691-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c691-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="1c691-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c691-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1c691-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1c691-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="1c691-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1c691-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1c691-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1c691-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1c691-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1c691-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1c691-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1c691-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="1c691-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1c691-112">recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="1c691-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c691-113">Définition</span><span class="sxs-lookup"><span data-stu-id="1c691-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c691-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1c691-114">Elements and attributes</span></span>

<span data-ttu-id="1c691-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1c691-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1c691-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1c691-116">Parent elements</span></span>

|<span data-ttu-id="1c691-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1c691-117">**Element**</span></span>|<span data-ttu-id="1c691-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c691-118">**Type**</span></span>|<span data-ttu-id="1c691-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c691-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c691-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="1c691-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c691-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="1c691-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c691-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="1c691-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1c691-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1c691-123">Child elements</span></span>

|<span data-ttu-id="1c691-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1c691-124">**Element**</span></span>|<span data-ttu-id="1c691-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c691-125">**Type**</span></span>|<span data-ttu-id="1c691-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c691-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c691-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="1c691-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c691-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="1c691-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c691-129">Spécifie la valeur de ce composant de la clé primaire pour une ligne d’un objet recordset.</span><span class="sxs-lookup"><span data-stu-id="1c691-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="1c691-130">Il doit exister au moins une occurrence de cet élément enfant.</span><span class="sxs-lookup"><span data-stu-id="1c691-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1c691-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="1c691-131">Attributes</span></span>

|<span data-ttu-id="1c691-132">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1c691-132">**Attribute**</span></span>|<span data-ttu-id="1c691-133">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c691-133">**Type**</span></span>|<span data-ttu-id="1c691-134">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1c691-134">**Required**</span></span>|<span data-ttu-id="1c691-135">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c691-135">**Description**</span></span>|<span data-ttu-id="1c691-136">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1c691-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c691-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="1c691-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="1c691-138">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1c691-138">xsd:string</span></span>  <br/> |<span data-ttu-id="1c691-139">facultatif</span><span class="sxs-lookup"><span data-stu-id="1c691-139">optional</span></span>  <br/> |<span data-ttu-id="1c691-140">Spécifie le nom d’un champ qui est un composant de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="1c691-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="1c691-141">Il doit être la valeur de l’attribut **ColumnNameID** d’un élément descendant DataColumn_Type de la DataRecordSet_Type dont la clé primaire est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1c691-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="1c691-142">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="1c691-142">Values of the xsd:string type.</span></span>  <br/> |
   

