---
title: ComplexType FooterMargin_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f5838855a5c21b699c7a81849b9afc40790f3d01
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538640"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="aad88-102">ComplexType FooterMargin_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aad88-102">FooterMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aad88-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="aad88-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aad88-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aad88-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aad88-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="aad88-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aad88-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="aad88-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aad88-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="aad88-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aad88-108">xsd: double</span><span class="sxs-lookup"><span data-stu-id="aad88-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aad88-109">Définition</span><span class="sxs-lookup"><span data-stu-id="aad88-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aad88-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="aad88-110">Elements and attributes</span></span>

<span data-ttu-id="aad88-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="aad88-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aad88-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aad88-112">Child elements</span></span>

<span data-ttu-id="aad88-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aad88-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aad88-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="aad88-114">Attributes</span></span>

|<span data-ttu-id="aad88-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aad88-115">**Attribute**</span></span>|<span data-ttu-id="aad88-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="aad88-116">**Type**</span></span>|<span data-ttu-id="aad88-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="aad88-117">**Required**</span></span>|<span data-ttu-id="aad88-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="aad88-118">**Description**</span></span>|<span data-ttu-id="aad88-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="aad88-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aad88-120">Unit</span><span class="sxs-lookup"><span data-stu-id="aad88-120">Unit</span></span>  <br/> |<span data-ttu-id="aad88-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="aad88-121">xsd:string</span></span>  <br/> |<span data-ttu-id="aad88-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="aad88-122">optional</span></span>  <br/> ||<span data-ttu-id="aad88-123">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aad88-123">Values of the xsd:string type.</span></span>  <br/> |
   

