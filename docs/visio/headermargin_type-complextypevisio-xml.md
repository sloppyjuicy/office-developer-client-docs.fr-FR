---
title: HeaderMargin_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 2d4a1fb15172d86a7843616679df4177d6f8292b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539088"
---
# <a name="headermargin_type-complextype-visio-xml"></a><span data-ttu-id="3676b-102">HeaderMargin_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3676b-102">HeaderMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3676b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3676b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3676b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3676b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3676b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3676b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3676b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3676b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3676b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3676b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3676b-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="3676b-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3676b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3676b-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3676b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3676b-110">Elements and attributes</span></span>

<span data-ttu-id="3676b-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="3676b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3676b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3676b-112">Child elements</span></span>

<span data-ttu-id="3676b-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3676b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3676b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3676b-114">Attributes</span></span>

|<span data-ttu-id="3676b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3676b-115">**Attribute**</span></span>|<span data-ttu-id="3676b-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="3676b-116">**Type**</span></span>|<span data-ttu-id="3676b-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3676b-117">**Required**</span></span>|<span data-ttu-id="3676b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="3676b-118">**Description**</span></span>|<span data-ttu-id="3676b-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3676b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3676b-120">Unit</span><span class="sxs-lookup"><span data-stu-id="3676b-120">Unit</span></span>  <br/> |<span data-ttu-id="3676b-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3676b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="3676b-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="3676b-122">optional</span></span>  <br/> ||<span data-ttu-id="3676b-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3676b-123">Values of the xsd:string type.</span></span>  <br/> |
   

