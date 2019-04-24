---
title: ComplexType RowDef_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355768"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="db8f7-102">ComplexType RowDef_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="db8f7-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="db8f7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="db8f7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db8f7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db8f7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="db8f7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="db8f7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="db8f7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="db8f7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="db8f7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="db8f7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="db8f7-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="db8f7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db8f7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="db8f7-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="db8f7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="db8f7-110">Elements and attributes</span></span>

<span data-ttu-id="db8f7-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="db8f7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="db8f7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="db8f7-112">Child elements</span></span>

|<span data-ttu-id="db8f7-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="db8f7-113">**Element**</span></span>|<span data-ttu-id="db8f7-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="db8f7-114">**Type**</span></span>|<span data-ttu-id="db8f7-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="db8f7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="db8f7-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="db8f7-116">CellDef</span></span> <br/> |[<span data-ttu-id="db8f7-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="db8f7-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="db8f7-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="db8f7-118">Attributes</span></span>

<span data-ttu-id="db8f7-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="db8f7-119">None.</span></span>
  

