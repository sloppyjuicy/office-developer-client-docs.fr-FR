---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540587"
---
# <a name="pagesheet_type-complextype-visio-xml"></a><span data-ttu-id="86b78-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="86b78-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="86b78-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="86b78-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86b78-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="86b78-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="86b78-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="86b78-105">**Schema file**</span></span> <br/> |<span data-ttu-id="86b78-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="86b78-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="86b78-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="86b78-107">**Extension base**</span></span> <br/> |<span data-ttu-id="86b78-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="86b78-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86b78-109">Définition</span><span class="sxs-lookup"><span data-stu-id="86b78-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86b78-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="86b78-110">Elements and attributes</span></span>

<span data-ttu-id="86b78-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="86b78-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="86b78-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="86b78-112">Child elements</span></span>

<span data-ttu-id="86b78-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="86b78-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86b78-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="86b78-114">Attributes</span></span>

|<span data-ttu-id="86b78-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="86b78-115">**Attribute**</span></span>|<span data-ttu-id="86b78-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="86b78-116">**Type**</span></span>|<span data-ttu-id="86b78-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="86b78-117">**Required**</span></span>|<span data-ttu-id="86b78-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="86b78-118">**Description**</span></span>|<span data-ttu-id="86b78-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="86b78-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="86b78-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="86b78-120">UniqueID</span></span>  <br/> |<span data-ttu-id="86b78-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86b78-121">xsd:string</span></span>  <br/> |<span data-ttu-id="86b78-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="86b78-122">optional</span></span>  <br/> ||<span data-ttu-id="86b78-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86b78-123">Values of the xsd:string type.</span></span>  <br/> |
   

