---
title: Élément RowKeyValue (complexType PrimaryKey_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Spécifie la valeur d’une clé primaire pour une ligne individuelle d’un objet Recordset.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538129"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="a0cf7-103">Élément RowKeyValue (complexType PrimaryKey_Type) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="a0cf7-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a0cf7-104">Spécifie la valeur d’une clé primaire pour une ligne individuelle d’un objet Recordset.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0cf7-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a0cf7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0cf7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a0cf7-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="a0cf7-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a0cf7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a0cf7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a0cf7-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a0cf7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a0cf7-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a0cf7-112">recordsets. Xml</span><span class="sxs-lookup"><span data-stu-id="a0cf7-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0cf7-113">Définition</span><span class="sxs-lookup"><span data-stu-id="a0cf7-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a0cf7-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a0cf7-114">Elements and attributes</span></span>

<span data-ttu-id="a0cf7-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a0cf7-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a0cf7-116">Parent elements</span></span>

|<span data-ttu-id="a0cf7-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-117">**Element**</span></span>|<span data-ttu-id="a0cf7-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-118">**Type**</span></span>|<span data-ttu-id="a0cf7-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0cf7-120">Primaire</span><span class="sxs-lookup"><span data-stu-id="a0cf7-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0cf7-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="a0cf7-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a0cf7-122">Spécifie une clé primaire d’un objet Recordset.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0cf7-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a0cf7-123">Child elements</span></span>

<span data-ttu-id="a0cf7-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0cf7-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="a0cf7-125">Attributes</span></span>

|<span data-ttu-id="a0cf7-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-126">**Attribute**</span></span>|<span data-ttu-id="a0cf7-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-127">**Type**</span></span>|<span data-ttu-id="a0cf7-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-128">**Required**</span></span>|<span data-ttu-id="a0cf7-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-129">**Description**</span></span>|<span data-ttu-id="a0cf7-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a0cf7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a0cf7-131">RowID</span><span class="sxs-lookup"><span data-stu-id="a0cf7-131">RowID</span></span>  <br/> |<span data-ttu-id="a0cf7-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a0cf7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a0cf7-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a0cf7-133">required</span></span>  <br/> |<span data-ttu-id="a0cf7-134">Valeur unique qui identifie une ligne d’un jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="a0cf7-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a0cf7-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0cf7-136">Value</span></span>  <br/> |<span data-ttu-id="a0cf7-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a0cf7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a0cf7-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a0cf7-138">required</span></span>  <br/> |<span data-ttu-id="a0cf7-139">Valeur de la clé primaire pour cette ligne de l’objet Recordset.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="a0cf7-140">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a0cf7-140">Values of the xsd:string type.</span></span>  <br/> |
   

