---
title: ComplexType FieldRow_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: f6102c89cc0e484b1a07fb11bf26285df8954a5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542358"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="6b74a-102">ComplexType FieldRow_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6b74a-102">FieldRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6b74a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6b74a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b74a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6b74a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6b74a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6b74a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6b74a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6b74a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6b74a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6b74a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6b74a-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="6b74a-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b74a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6b74a-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b74a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6b74a-110">Elements and attributes</span></span>

<span data-ttu-id="6b74a-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="6b74a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6b74a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6b74a-112">Child elements</span></span>

|<span data-ttu-id="6b74a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6b74a-113">**Element**</span></span>|<span data-ttu-id="6b74a-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6b74a-114">**Type**</span></span>|<span data-ttu-id="6b74a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6b74a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b74a-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6b74a-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6b74a-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6b74a-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6b74a-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6b74a-118">Attributes</span></span>

<span data-ttu-id="6b74a-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6b74a-119">None.</span></span>
  

