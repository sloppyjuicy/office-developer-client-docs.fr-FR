---
title: ComplexType ActionsRow_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32777219-850b-9526-425f-bcb017c45093
ms.openlocfilehash: d62513877dc2c441d521b20505f5849ea31a1a4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283002"
---
# <a name="actionsrowtype-complextype-visio-xml"></a><span data-ttu-id="85859-102">ComplexType ActionsRow_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="85859-102">ActionsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85859-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="85859-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85859-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85859-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85859-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="85859-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85859-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="85859-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85859-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="85859-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85859-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="85859-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85859-109">Définition</span><span class="sxs-lookup"><span data-stu-id="85859-109">Definition</span></span>

```XML
          <xs:complexType name="ActionsRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="85859-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="85859-110">Elements and attributes</span></span>

<span data-ttu-id="85859-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="85859-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85859-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="85859-112">Child elements</span></span>

|<span data-ttu-id="85859-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="85859-113">**Element**</span></span>|<span data-ttu-id="85859-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="85859-114">**Type**</span></span>|<span data-ttu-id="85859-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="85859-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85859-116">Cell</span><span class="sxs-lookup"><span data-stu-id="85859-116">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="85859-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="85859-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85859-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="85859-118">Attributes</span></span>

<span data-ttu-id="85859-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="85859-119">None.</span></span>
  

