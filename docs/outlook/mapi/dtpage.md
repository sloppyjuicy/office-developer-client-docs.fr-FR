---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287104"
---
# <a name="dtpage"></a><span data-ttu-id="24fef-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="24fef-103">DTPAGE</span></span>

  
  
<span data-ttu-id="24fef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24fef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24fef-105">Décrit la boîte de dialogue qui est générée à partir d'une table d'affichage par la fonction [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="24fef-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24fef-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="24fef-106">Header file:</span></span>  <br/> |<span data-ttu-id="24fef-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="24fef-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="24fef-108">Members</span><span class="sxs-lookup"><span data-stu-id="24fef-108">Members</span></span>

 <span data-ttu-id="24fef-109">**CCTL**</span><span class="sxs-lookup"><span data-stu-id="24fef-109">**cctl**</span></span>
  
> <span data-ttu-id="24fef-110">Nombre de contrôles vers lesquels pointe le membre **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="24fef-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="24fef-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="24fef-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="24fef-112">Pointeur vers le nom ou l'identificateur entier de la ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="24fef-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="24fef-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="24fef-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="24fef-114">Pointeur vers la chaîne qui apparaît dans la section **[Help file Mappings] du fichier** MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="24fef-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="24fef-115">Étant donné que **lpszComponent** est dans une Union avec le membre **ulItemID** , un seul de ces membres a des données valides.</span><span class="sxs-lookup"><span data-stu-id="24fef-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="24fef-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="24fef-116">**ulItemID**</span></span>
  
> <span data-ttu-id="24fef-117">Identificateur de ressource entier avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom du fichier d'aide peut être lu.</span><span class="sxs-lookup"><span data-stu-id="24fef-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="24fef-118">Étant donné que **ulItemID** est dans une Union avec le membre **lpszComponent** , un seul de ces membres a des données valides.</span><span class="sxs-lookup"><span data-stu-id="24fef-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="24fef-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="24fef-119">**lpctl**</span></span>
  
> <span data-ttu-id="24fef-120">Pointeur vers un tableau de structures [DTCTL](dtctl.md) , un pour chaque contrôle sur la page.</span><span class="sxs-lookup"><span data-stu-id="24fef-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24fef-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="24fef-121">Remarks</span></span>

<span data-ttu-id="24fef-122">Pour identifier le fichier d'aide de la page à onglets, définissez le membre **lpszComponent** sur une chaîne codée en dur ou le membre **ulItemID** sur un identificateur de ressource Integer.</span><span class="sxs-lookup"><span data-stu-id="24fef-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="24fef-123">Chaque entrée de la section **[Help file Mappings]** dans MAPISVC. INF se compose d'une chaîne de composant, pas de plus de 30 caractères, du côté gauche et d'un chemin d'accès au fichier d'aide à droite.</span><span class="sxs-lookup"><span data-stu-id="24fef-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="24fef-124">**UlItemID** et **lpszResourceName** sont trouvés dans le paramètre _HINSTANCE_ de **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="24fef-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="24fef-125">Pour plus d'informations, consultez la rubrique [MAPISVC. Section INF [mappages de fichiers d'aide]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="24fef-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="24fef-126">Bien que **BuildDisplayTable** utilise cette structure pour créer la table d'affichage à partir des ressources de contrôle, la structure **DTPAGE** n'apparaît jamais dans le tableau proprement dit.</span><span class="sxs-lookup"><span data-stu-id="24fef-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="24fef-127">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="24fef-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="24fef-128">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="24fef-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24fef-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24fef-129">See also</span></span>



[<span data-ttu-id="24fef-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="24fef-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="24fef-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="24fef-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="24fef-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="24fef-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="24fef-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="24fef-133">MAPI Structures</span></span>](mapi-structures.md)

