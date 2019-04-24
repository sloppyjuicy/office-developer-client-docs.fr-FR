---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299516"
---
# <a name="guid"></a><span data-ttu-id="1d130-103">GUID</span><span class="sxs-lookup"><span data-stu-id="1d130-103">GUID</span></span>

  
  
<span data-ttu-id="1d130-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d130-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d130-105">Décrit un identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="1d130-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d130-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1d130-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d130-107">Mapiguid. h</span><span class="sxs-lookup"><span data-stu-id="1d130-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="1d130-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d130-108">Members</span></span>

 <span data-ttu-id="1d130-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="1d130-109">**Data1**</span></span>
  
> <span data-ttu-id="1d130-110">Valeur de type long Integer non signée.</span><span class="sxs-lookup"><span data-stu-id="1d130-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="1d130-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="1d130-111">**Data2**</span></span>
  
> <span data-ttu-id="1d130-112">Valeur de type Integer courte non signée.</span><span class="sxs-lookup"><span data-stu-id="1d130-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="1d130-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="1d130-113">**Data3**</span></span>
  
> <span data-ttu-id="1d130-114">Valeur de type Integer courte non signée.</span><span class="sxs-lookup"><span data-stu-id="1d130-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="1d130-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="1d130-115">**Data4**</span></span>
  
> <span data-ttu-id="1d130-116">Tableau de caractères non signés.</span><span class="sxs-lookup"><span data-stu-id="1d130-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d130-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d130-117">Remarks</span></span>

 <span data-ttu-id="1d130-118">Les structures de **GUID** sont utilisées dans MAPI de la manière suivante:</span><span class="sxs-lookup"><span data-stu-id="1d130-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="1d130-119">Dans les structures [MAPIUID](mapiuid.md) qui identifient les fournisseurs de services de manière unique.</span><span class="sxs-lookup"><span data-stu-id="1d130-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="1d130-120">Pour les identificateurs d'interface.</span><span class="sxs-lookup"><span data-stu-id="1d130-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="1d130-121">Dans le jeu de propriétés, définissez les noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="1d130-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="1d130-122">Banque de messages et fournisseurs de carnet d'adresses génèrent une structure de **GUID** à utiliser dans leur structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="1d130-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="1d130-123">En transmettant le **MAPIUID** résultant à [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="1d130-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="1d130-124">En outre, elles sont utilisées dans l'implémentation de l'appel de procédure disTante (RPC) Microsoft et du langage ODL (Object Description Language).</span><span class="sxs-lookup"><span data-stu-id="1d130-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="1d130-125">Pour plus d'informations sur ces utilisations \*\* , reportez-vous au *Guide de référence du programmeur RPC Microsoft et*à l' *intérieur OLE*, *deuxième édition* .</span><span class="sxs-lookup"><span data-stu-id="1d130-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="1d130-126">La structure du **GUID** est définie dans le *Guide de référence du programmeur Win32* .</span><span class="sxs-lookup"><span data-stu-id="1d130-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="1d130-127">Les valeurs spécifiques des structures de **GUID** utilisées dans MAPI sont définies dans le fichier d'en-tête MAPI Mapiguid. h.</span><span class="sxs-lookup"><span data-stu-id="1d130-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d130-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d130-128">See also</span></span>



[<span data-ttu-id="1d130-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1d130-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="1d130-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="1d130-130">MAPI Structures</span></span>](mapi-structures.md)

