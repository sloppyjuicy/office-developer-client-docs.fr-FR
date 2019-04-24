---
title: ComplexType UserRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 54edb9a1396582eae87db8735c4f75bd9597f1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337071"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="96510-102">ComplexType UserRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="96510-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="96510-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="96510-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96510-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="96510-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="96510-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="96510-105">**Schema file**</span></span> <br/> |<span data-ttu-id="96510-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="96510-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="96510-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="96510-107">**Extension base**</span></span> <br/> |<span data-ttu-id="96510-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="96510-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96510-109">Définition</span><span class="sxs-lookup"><span data-stu-id="96510-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="96510-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="96510-110">Elements and attributes</span></span>

<span data-ttu-id="96510-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="96510-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="96510-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="96510-112">Child elements</span></span>

|<span data-ttu-id="96510-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="96510-113">**Element**</span></span>|<span data-ttu-id="96510-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="96510-114">**Type**</span></span>|<span data-ttu-id="96510-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="96510-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96510-116">Cell</span><span class="sxs-lookup"><span data-stu-id="96510-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="96510-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="96510-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="96510-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="96510-118">Attributes</span></span>

<span data-ttu-id="96510-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="96510-119">None.</span></span>
  

