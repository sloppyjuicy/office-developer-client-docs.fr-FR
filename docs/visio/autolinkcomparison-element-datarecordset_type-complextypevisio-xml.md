---
title: Élément AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Définit une règle qui compare une colonne de l’élément DataRecordset parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537870"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="d0cd4-103">Élément AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d0cd4-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d0cd4-104">Définit une règle qui compare une colonne de l’élément **DataRecordset** parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d0cd4-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d0cd4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0cd4-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d0cd4-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="d0cd4-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d0cd4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d0cd4-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d0cd4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d0cd4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d0cd4-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d0cd4-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="d0cd4-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0cd4-113">Définition</span><span class="sxs-lookup"><span data-stu-id="d0cd4-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0cd4-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d0cd4-114">Elements and attributes</span></span>

<span data-ttu-id="d0cd4-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d0cd4-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d0cd4-116">Parent elements</span></span>

|<span data-ttu-id="d0cd4-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-117">**Element**</span></span>|<span data-ttu-id="d0cd4-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-118">**Type**</span></span>|<span data-ttu-id="d0cd4-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0cd4-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="d0cd4-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0cd4-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="d0cd4-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0cd4-122">Spécifie un recordset et la liaison de données entre ce recordset et les formes dans les pages de dessin.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d0cd4-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d0cd4-123">Child elements</span></span>

<span data-ttu-id="d0cd4-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0cd4-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="d0cd4-125">Attributes</span></span>

|<span data-ttu-id="d0cd4-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-126">**Attribute**</span></span>|<span data-ttu-id="d0cd4-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-127">**Type**</span></span>|<span data-ttu-id="d0cd4-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-128">**Required**</span></span>|<span data-ttu-id="d0cd4-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-129">**Description**</span></span>|<span data-ttu-id="d0cd4-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d0cd4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0cd4-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="d0cd4-131">ColumnName</span></span>  <br/> |<span data-ttu-id="d0cd4-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0cd4-132">xsd:string</span></span>  <br/> |<span data-ttu-id="d0cd4-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0cd4-133">required</span></span>  <br/> |<span data-ttu-id="d0cd4-134">Correspond à un nom de colonne dans le recordset ADO.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="d0cd4-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0cd4-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="d0cd4-136">ContextType</span></span>  <br/> |<span data-ttu-id="d0cd4-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0cd4-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0cd4-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0cd4-138">required</span></span>  <br/> |<span data-ttu-id="d0cd4-139">Spécifie les propriétés du groupe ou de la forme à utiliser pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="d0cd4-140">Les valeurs possibles sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="d0cd4-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0cd4-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="d0cd4-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="d0cd4-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0cd4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d0cd4-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="d0cd4-144">optional</span></span>  <br/> |<span data-ttu-id="d0cd4-145">Si la valeur ContextType est 2 ou 3, cet attribut est requis pour définir une comparaison.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="d0cd4-146">Pour ContextType = 2, ContextTypeLabel doit être l’étiquette de l’élément de données de forme, et si **ContextType** = 3, ContextTypeLabel doit être le nom de ligne local.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="d0cd4-147">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d0cd4-147">Values of the xsd:string type.</span></span>  <br/> |
   

