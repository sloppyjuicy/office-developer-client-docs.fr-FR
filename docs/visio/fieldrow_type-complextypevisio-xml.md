---
title: ComplexType FieldRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: 5f59ca23fa83d98622624cc20544f9b482ce5378
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322560"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="7b5f1-102">ComplexType FieldRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7b5f1-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b5f1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7b5f1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b5f1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b5f1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b5f1-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7b5f1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b5f1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b5f1-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="7b5f1-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b5f1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7b5f1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7b5f1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7b5f1-110">Elements and attributes</span></span>

<span data-ttu-id="7b5f1-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7b5f1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b5f1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7b5f1-112">Child elements</span></span>

|<span data-ttu-id="7b5f1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-113">**Element**</span></span>|<span data-ttu-id="7b5f1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-114">**Type**</span></span>|<span data-ttu-id="7b5f1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b5f1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b5f1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="7b5f1-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7b5f1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7b5f1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7b5f1-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="7b5f1-118">Attributes</span></span>

<span data-ttu-id="7b5f1-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7b5f1-119">None.</span></span>
  

