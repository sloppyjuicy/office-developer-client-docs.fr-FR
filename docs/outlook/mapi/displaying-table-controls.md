---
title: Affichage des contrôles de tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422690"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="023cd-103">Affichage des contrôles de tableau</span><span class="sxs-lookup"><span data-stu-id="023cd-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="023cd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="023cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="023cd-105">Il existe de nombreux types de contrôles différents, aucun propre à MAPI.</span><span class="sxs-lookup"><span data-stu-id="023cd-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="023cd-106">Toutefois, MAPI définit ses propres structures utilisées conjointement avec [BuildDisplayTable](builddisplaytable.md) pour décrire l’ensemble unique de données impliquées dans chaque contrôle.</span><span class="sxs-lookup"><span data-stu-id="023cd-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="023cd-107">Le tableau suivant répertorie les structures qui décrivent chaque type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="023cd-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="023cd-108">**Structure des contrôles**</span><span class="sxs-lookup"><span data-stu-id="023cd-108">**Control structure**</span></span>|<span data-ttu-id="023cd-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="023cd-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="023cd-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="023cd-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="023cd-111">Décrit un contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="023cd-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="023cd-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="023cd-113">Décrit un contrôle case à cocher.</span><span class="sxs-lookup"><span data-stu-id="023cd-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="023cd-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="023cd-115">Décrit un contrôle de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="023cd-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="023cd-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="023cd-117">Décrit un contrôle de zone de liste liste.</span><span class="sxs-lookup"><span data-stu-id="023cd-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="023cd-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="023cd-119">Décrit un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="023cd-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="023cd-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="023cd-121">Décrit un contrôle de zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="023cd-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="023cd-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="023cd-123">Décrit un contrôle d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="023cd-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="023cd-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="023cd-125">Décrit un contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="023cd-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="023cd-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="023cd-127">Décrit un contrôle de zone de liste rouge à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="023cd-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="023cd-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="023cd-129">Décrit un contrôle de zone de liste à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="023cd-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="023cd-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="023cd-131">Décrit un contrôle de page à onglets.</span><span class="sxs-lookup"><span data-stu-id="023cd-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="023cd-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="023cd-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="023cd-133">Décrit un contrôle de bouton d’option.</span><span class="sxs-lookup"><span data-stu-id="023cd-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="023cd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="023cd-134">See also</span></span>



[<span data-ttu-id="023cd-135">Implémentation du tableau d’affichage</span><span class="sxs-lookup"><span data-stu-id="023cd-135">Display Table Implementation</span></span>](display-table-implementation.md)

