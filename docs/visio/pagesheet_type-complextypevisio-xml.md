---
title: ComplexType PageSheet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334649"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="1eaa7-102">ComplexType PageSheet_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1eaa7-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1eaa7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1eaa7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1eaa7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1eaa7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1eaa7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1eaa7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1eaa7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1eaa7-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="1eaa7-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1eaa7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1eaa7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1eaa7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1eaa7-110">Elements and attributes</span></span>

<span data-ttu-id="1eaa7-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="1eaa7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1eaa7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1eaa7-112">Child elements</span></span>

<span data-ttu-id="1eaa7-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1eaa7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1eaa7-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1eaa7-114">Attributes</span></span>

|<span data-ttu-id="1eaa7-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-115">**Attribute**</span></span>|<span data-ttu-id="1eaa7-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-116">**Type**</span></span>|<span data-ttu-id="1eaa7-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-117">**Required**</span></span>|<span data-ttu-id="1eaa7-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-118">**Description**</span></span>|<span data-ttu-id="1eaa7-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1eaa7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1eaa7-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="1eaa7-120">UniqueID</span></span>  <br/> |<span data-ttu-id="1eaa7-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1eaa7-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1eaa7-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="1eaa7-122">optional</span></span>  <br/> ||<span data-ttu-id="1eaa7-123">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1eaa7-123">Values of the xsd:string type.</span></span>  <br/> |
   

