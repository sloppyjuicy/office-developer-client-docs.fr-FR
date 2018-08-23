---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583343"
---
# <a name="direntryid"></a><span data-ttu-id="62a81-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="62a81-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="62a81-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62a81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62a81-105">Décrit les propriétés de l’id d’entrée de répertoire.</span><span class="sxs-lookup"><span data-stu-id="62a81-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62a81-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="62a81-106">Header file:</span></span>  <br/> |<span data-ttu-id="62a81-107">EntryID.h</span><span class="sxs-lookup"><span data-stu-id="62a81-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="62a81-108">Members</span><span class="sxs-lookup"><span data-stu-id="62a81-108">Members</span></span>

 <span data-ttu-id="62a81-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="62a81-109">**abFlags**</span></span>
  
> <span data-ttu-id="62a81-110">Masque de bits d’indicateurs qui fournit des informations décrivant l’objet.</span><span class="sxs-lookup"><span data-stu-id="62a81-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="62a81-111">Pour plus d’informations, voir la description du champ **abFlags** d’une structure [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="62a81-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="62a81-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="62a81-112">**muid**</span></span>
  
> <span data-ttu-id="62a81-113">GUID qui identifie le fournisseur de banque.</span><span class="sxs-lookup"><span data-stu-id="62a81-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="62a81-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="62a81-114">**ulVersion**</span></span>
  
> <span data-ttu-id="62a81-115">Le numéro de version de la structure **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="62a81-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="62a81-116">Doit être défini sur CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="62a81-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="62a81-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="62a81-117">**ulType**</span></span>
  
> <span data-ttu-id="62a81-118">Nombre entier représentant le type d’ID de l’entrée directory.</span><span class="sxs-lookup"><span data-stu-id="62a81-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="62a81-119">Il doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="62a81-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="62a81-120">**Nom**</span><span class="sxs-lookup"><span data-stu-id="62a81-120">**Name**</span></span>|<span data-ttu-id="62a81-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a81-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62a81-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="62a81-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="62a81-123">Le dossier racine d’un carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="62a81-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="62a81-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="62a81-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="62a81-125">Un sous-dossier contenu dans le dossier racine de l’objet de carnet d’adresses MAPI.</span><span class="sxs-lookup"><span data-stu-id="62a81-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="62a81-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="62a81-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="62a81-127">Un objet conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="62a81-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="62a81-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="62a81-128">**muidID**</span></span>
  
> <span data-ttu-id="62a81-129">GUID qui identifie l’objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="62a81-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62a81-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="62a81-130">Remarks</span></span>

<span data-ttu-id="62a81-131">Les structures **DIR_ENTRYID** et [CONTAB_ENTRYID](contab_entryid.md) sont identiques, à l’exception du membre **ulType** .</span><span class="sxs-lookup"><span data-stu-id="62a81-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="62a81-132">Le contenu du membre **ulType** détermine dont la structure est appropriée pour les champs restants.</span><span class="sxs-lookup"><span data-stu-id="62a81-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62a81-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a81-133">See also</span></span>



[<span data-ttu-id="62a81-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="62a81-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="62a81-135">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="62a81-135">MAPI Structures</span></span>](mapi-structures.md)

