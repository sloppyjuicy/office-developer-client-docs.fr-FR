---
title: Affichage des contrôles de Table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783194"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="82887-103">Affichage des contrôles de Table</span><span class="sxs-lookup"><span data-stu-id="82887-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="82887-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82887-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82887-105">Il existe de nombreux types de contrôles, aucun unique à MAPI.</span><span class="sxs-lookup"><span data-stu-id="82887-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="82887-106">Toutefois, MAPI définit ses propres structures qui sont utilisés conjointement avec [BuildDisplayTable](builddisplaytable.md) pour décrire le jeu de données à chaque contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="82887-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="82887-107">Le tableau suivant répertorie les structures qui décrivent chaque type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="82887-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="82887-108">**Structure de contrôle**</span><span class="sxs-lookup"><span data-stu-id="82887-108">**Control structure**</span></span>|<span data-ttu-id="82887-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="82887-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82887-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="82887-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="82887-111">Décrit un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="82887-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="82887-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="82887-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="82887-113">Décrit un contrôle de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="82887-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="82887-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="82887-115">Décrit un contrôle de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="82887-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="82887-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="82887-117">Décrit un contrôle de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="82887-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="82887-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="82887-119">Décrit un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="82887-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="82887-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="82887-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="82887-121">Décrit un contrôle de zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="82887-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="82887-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="82887-123">Décrit un contrôle label.</span><span class="sxs-lookup"><span data-stu-id="82887-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="82887-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="82887-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="82887-125">Décrit un contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="82887-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="82887-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="82887-127">Décrit un contrôle de zone de liste déroulante de plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="82887-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="82887-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="82887-129">Décrit un contrôle de zone de liste de plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="82887-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="82887-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="82887-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="82887-131">Décrit un contrôle de la page à onglets.</span><span class="sxs-lookup"><span data-stu-id="82887-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="82887-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="82887-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="82887-133">Décrit un contrôle bouton d’option.</span><span class="sxs-lookup"><span data-stu-id="82887-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82887-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82887-134">See also</span></span>



[<span data-ttu-id="82887-135">Affichage tableau implémentation</span><span class="sxs-lookup"><span data-stu-id="82887-135">Display Table Implementation</span></span>](display-table-implementation.md)

