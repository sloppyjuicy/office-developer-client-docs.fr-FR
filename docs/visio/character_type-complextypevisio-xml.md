---
title: ComplexType Character_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: d4145bf92c053f67ed11e827b528e05fd4ffc7f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341866"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="ab219-102">ComplexType Character_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ab219-102">Character_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ab219-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ab219-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab219-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab219-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ab219-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ab219-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ab219-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ab219-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ab219-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ab219-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ab219-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ab219-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab219-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ab219-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ab219-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ab219-110">Elements and attributes</span></span>

<span data-ttu-id="ab219-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ab219-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab219-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ab219-112">Child elements</span></span>

|<span data-ttu-id="ab219-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ab219-113">**Element**</span></span>|<span data-ttu-id="ab219-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ab219-114">**Type**</span></span>|<span data-ttu-id="ab219-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab219-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab219-116">Row</span><span class="sxs-lookup"><span data-stu-id="ab219-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ab219-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="ab219-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ab219-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ab219-118">Attributes</span></span>

<span data-ttu-id="ab219-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ab219-119">None.</span></span>
  

