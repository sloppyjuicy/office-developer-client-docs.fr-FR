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
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783424"
---
# <a name="guid"></a><span data-ttu-id="8a3d5-103">GUID</span><span class="sxs-lookup"><span data-stu-id="8a3d5-103">GUID</span></span>

  
  
<span data-ttu-id="8a3d5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a3d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a3d5-105">Décrit un identificateur global unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="8a3d5-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a3d5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8a3d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="8a3d5-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="8a3d5-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="8a3d5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8a3d5-108">Members</span></span>

 <span data-ttu-id="8a3d5-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="8a3d5-109">**Data1**</span></span>
  
> <span data-ttu-id="8a3d5-110">Une valeur de données entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="8a3d5-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="8a3d5-111">**Data2**</span></span>
  
> <span data-ttu-id="8a3d5-112">Une valeur de données entier court non signé.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="8a3d5-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="8a3d5-113">**Data3**</span></span>
  
> <span data-ttu-id="8a3d5-114">Une valeur de données entier court non signé.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="8a3d5-115">**Données4**</span><span class="sxs-lookup"><span data-stu-id="8a3d5-115">**Data4**</span></span>
  
> <span data-ttu-id="8a3d5-116">Un tableau de caractères non signés.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a3d5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a3d5-117">Remarks</span></span>

 <span data-ttu-id="8a3d5-118">Structures **GUID** sont utilisés dans MAPI comme suit :</span><span class="sxs-lookup"><span data-stu-id="8a3d5-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="8a3d5-119">Dans les structures [MAPIUID](mapiuid.md) qui identifient les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="8a3d5-120">Pour les identificateurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="8a3d5-121">Dans la propriété définie les noms des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="8a3d5-122">Banque de messages et l’adresse génèrent des fournisseurs de carnet d’une structure **GUID** à utiliser dans leur structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="8a3d5-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="8a3d5-123">En transmettant le résultant **MAPIUID** à [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="8a3d5-124">En outre, ils sont utilisés dans l’implémentation du service d’appel de procédure distante (RPC) Microsoft et de l’objet Description Language (ODL).</span><span class="sxs-lookup"><span data-stu-id="8a3d5-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="8a3d5-125">Pour plus d’informations sur ces utilisations, voir la *référence et le Guide du programmeur Microsoft RPC*, *référence du programmeur OLE* et *à l’intérieur de OLE*, *Deuxième Édition* .</span><span class="sxs-lookup"><span data-stu-id="8a3d5-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="8a3d5-126">La structure **GUID** est définie dans la *référence du programmeur Win32* .</span><span class="sxs-lookup"><span data-stu-id="8a3d5-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="8a3d5-127">Valeurs spécifiques pour les structures **GUID** qui sont utilisés dans MAPI sont définies dans le fichier d’en-tête Mapiguid.h MAPI.</span><span class="sxs-lookup"><span data-stu-id="8a3d5-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a3d5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a3d5-128">See also</span></span>



[<span data-ttu-id="8a3d5-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8a3d5-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="8a3d5-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3d5-130">MAPI Structures</span></span>](mapi-structures.md)

