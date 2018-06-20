---
title: Élément AutoLinkComparison (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Définit une règle qui compare une colonne dans l’élément DataRecordset parent avec un élément de données de forme à partir de la dernière réussite automatique liaison action effectuée dans l’interface utilisateur.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788046"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="97601-103">Élément AutoLinkComparison (DataRecordSet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="97601-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="97601-104">Définit une règle qui compare une colonne dans l’élément **DataRecordset** parent avec un élément de données de forme à partir de la dernière réussite automatique liaison action effectuée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97601-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="97601-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="97601-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97601-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="97601-106">**Element type**</span></span> <br/> |[<span data-ttu-id="97601-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="97601-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="97601-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="97601-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="97601-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="97601-109">**Schema file**</span></span> <br/> |<span data-ttu-id="97601-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="97601-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="97601-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="97601-111">**Document parts**</span></span> <br/> |<span data-ttu-id="97601-112">recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="97601-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="97601-113">Définition</span><span class="sxs-lookup"><span data-stu-id="97601-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="97601-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="97601-114">Elements and attributes</span></span>

<span data-ttu-id="97601-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="97601-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="97601-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="97601-116">Parent elements</span></span>

|<span data-ttu-id="97601-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="97601-117">**Element**</span></span>|<span data-ttu-id="97601-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="97601-118">**Type**</span></span>|<span data-ttu-id="97601-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="97601-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97601-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="97601-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="97601-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="97601-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="97601-122">Spécifie un jeu d’enregistrements et la liaison de données entre ce jeu d’enregistrements et les formes dans les pages de dessin.</span><span class="sxs-lookup"><span data-stu-id="97601-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97601-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="97601-123">Child elements</span></span>

<span data-ttu-id="97601-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="97601-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97601-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="97601-125">Attributes</span></span>

|<span data-ttu-id="97601-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="97601-126">**Attribute**</span></span>|<span data-ttu-id="97601-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="97601-127">**Type**</span></span>|<span data-ttu-id="97601-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="97601-128">**Required**</span></span>|<span data-ttu-id="97601-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="97601-129">**Description**</span></span>|<span data-ttu-id="97601-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="97601-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="97601-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="97601-131">ColumnName</span></span>  <br/> |<span data-ttu-id="97601-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="97601-132">xsd:string</span></span>  <br/> |<span data-ttu-id="97601-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="97601-133">required</span></span>  <br/> |<span data-ttu-id="97601-134">Correspond à un nom de colonne dans le jeu d’enregistrements ADO.</span><span class="sxs-lookup"><span data-stu-id="97601-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="97601-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="97601-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="97601-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="97601-136">ContextType</span></span>  <br/> |<span data-ttu-id="97601-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="97601-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="97601-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="97601-138">required</span></span>  <br/> |<span data-ttu-id="97601-139">Spécifie les propriétés de la forme ou un groupe à utiliser pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="97601-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="97601-140">Les valeurs sont présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="97601-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="97601-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="97601-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="97601-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="97601-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="97601-143">XSD : String</span><span class="sxs-lookup"><span data-stu-id="97601-143">xsd:string</span></span>  <br/> |<span data-ttu-id="97601-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="97601-144">optional</span></span>  <br/> |<span data-ttu-id="97601-145">Si la valeur ContextType est 2 ou 3, cet attribut est requis pour définir une comparaison.</span><span class="sxs-lookup"><span data-stu-id="97601-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="97601-146">Pour ContextType = 2, ContextTypeLabel doit être l’étiquette d’élément de données de forme et si **ContextType** = 3, ContextTypeLabel doit être le nom de ligne locale.</span><span class="sxs-lookup"><span data-stu-id="97601-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="97601-147">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="97601-147">Values of the xsd:string type.</span></span>  <br/> |
   

