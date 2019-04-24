---
title: ComplexType Actions_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283050"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="95eb8-102">ComplexType Actions_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="95eb8-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="95eb8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="95eb8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95eb8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95eb8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="95eb8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="95eb8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="95eb8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="95eb8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="95eb8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="95eb8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="95eb8-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="95eb8-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95eb8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="95eb8-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95eb8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="95eb8-110">Elements and attributes</span></span>

<span data-ttu-id="95eb8-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="95eb8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="95eb8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="95eb8-112">Child elements</span></span>

|<span data-ttu-id="95eb8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="95eb8-113">**Element**</span></span>|<span data-ttu-id="95eb8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="95eb8-114">**Type**</span></span>|<span data-ttu-id="95eb8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="95eb8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95eb8-116">Row</span><span class="sxs-lookup"><span data-stu-id="95eb8-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="95eb8-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="95eb8-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="95eb8-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="95eb8-118">Attributes</span></span>

<span data-ttu-id="95eb8-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="95eb8-119">None.</span></span>
  

