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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589671"
---
# <a name="dtpage"></a><span data-ttu-id="8be53-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="8be53-103">DTPAGE</span></span>

  
  
<span data-ttu-id="8be53-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8be53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8be53-105">Décrit la boîte de dialogue qui est générée à partir d’une table d’affichage par la fonction [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="8be53-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8be53-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8be53-106">Header file:</span></span>  <br/> |<span data-ttu-id="8be53-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8be53-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="8be53-108">Members</span><span class="sxs-lookup"><span data-stu-id="8be53-108">Members</span></span>

 <span data-ttu-id="8be53-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="8be53-109">**cctl**</span></span>
  
> <span data-ttu-id="8be53-110">Nombre de contrôles vers laquelle pointe le membre **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="8be53-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="8be53-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="8be53-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="8be53-112">Pointeur vers l’identificateur de nom ou entier de la ressource de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8be53-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="8be53-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="8be53-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="8be53-114">Pointeur vers la chaîne qui s’affiche dans la section **[Help File Mappings]** dans MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="8be53-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="8be53-115">**LpszComponent** étant une union avec le membre **ulItemID** , une seule de ces membres comporte des données valides.</span><span class="sxs-lookup"><span data-stu-id="8be53-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="8be53-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="8be53-116">**ulItemID**</span></span>
  
> <span data-ttu-id="8be53-117">Identificateur de ressources entier avec une valeur inférieure ou égale à 65535 à partir de laquelle le nom de fichier peut être lue.</span><span class="sxs-lookup"><span data-stu-id="8be53-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="8be53-118">**UlItemID** étant une union avec le membre **lpszComponent** , une seule de ces membres comporte des données valides.</span><span class="sxs-lookup"><span data-stu-id="8be53-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="8be53-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="8be53-119">**lpctl**</span></span>
  
> <span data-ttu-id="8be53-120">Pointeur vers un tableau de structures [DTCTL](dtctl.md) , un pour chaque contrôle sur la page.</span><span class="sxs-lookup"><span data-stu-id="8be53-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8be53-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8be53-121">Remarks</span></span>

<span data-ttu-id="8be53-122">Pour identifier le fichier d’aide pour la page à onglets, affectez le membre **lpszComponent** en chaîne codée en dur ou le membre **ulItemID** un identificateur de ressource entier.</span><span class="sxs-lookup"><span data-stu-id="8be53-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="8be53-123">Chaque entrée dans la section **[Help File Mappings]** dans le fichier MAPISVC.inf. INF se compose d’une chaîne de composant, pas plue de 30 caractères, sur le côté gauche et un chemin de fichier d’aide sur la droite.</span><span class="sxs-lookup"><span data-stu-id="8be53-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="8be53-124">À la fois **ulItemID** et **lpszResourceName** sont trouvent dans le paramètre _hInstance_ de **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="8be53-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="8be53-125">Pour plus d’informations, voir [fichier MAPISVC.inf. INF [aide File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="8be53-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="8be53-126">Bien que **BuildDisplayTable** utilise cette structure pour créer le tableau d’affichage de ressources du contrôle, la structure **DTPAGE** n’apparaît jamais dans la table d’affichage lui-même.</span><span class="sxs-lookup"><span data-stu-id="8be53-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="8be53-127">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8be53-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="8be53-128">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="8be53-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8be53-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8be53-129">See also</span></span>



[<span data-ttu-id="8be53-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="8be53-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="8be53-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="8be53-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="8be53-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="8be53-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="8be53-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8be53-133">MAPI Structures</span></span>](mapi-structures.md)

