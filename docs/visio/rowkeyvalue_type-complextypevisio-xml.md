---
title: Type complexe RowKeyValue_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387684"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="7337f-102">Type complexe RowKeyValue_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7337f-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7337f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7337f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7337f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7337f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7337f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7337f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7337f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7337f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7337f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7337f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7337f-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="7337f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7337f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7337f-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7337f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7337f-110">Elements and attributes</span></span>

<span data-ttu-id="7337f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7337f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7337f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7337f-112">Child elements</span></span>

<span data-ttu-id="7337f-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7337f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7337f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="7337f-114">Attributes</span></span>

|<span data-ttu-id="7337f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7337f-115">**Attribute**</span></span>|<span data-ttu-id="7337f-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="7337f-116">**Type**</span></span>|<span data-ttu-id="7337f-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7337f-117">**Required**</span></span>|<span data-ttu-id="7337f-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7337f-118">**Description**</span></span>|<span data-ttu-id="7337f-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7337f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7337f-120">RowID</span><span class="sxs-lookup"><span data-stu-id="7337f-120">RowID</span></span>  <br/> |<span data-ttu-id="7337f-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7337f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7337f-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7337f-122">required</span></span>  <br/> ||<span data-ttu-id="7337f-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7337f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7337f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7337f-124">Value</span></span>  <br/> |<span data-ttu-id="7337f-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="7337f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7337f-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7337f-126">required</span></span>  <br/> ||<span data-ttu-id="7337f-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="7337f-127">Values of the xsd:string type.</span></span>  <br/> |
   

