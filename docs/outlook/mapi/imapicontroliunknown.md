---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566515"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="a04cf-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a04cf-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="a04cf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a04cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a04cf-105">Permet de désactive un contrôle bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé.</span><span class="sxs-lookup"><span data-stu-id="a04cf-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="a04cf-106">Fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que des feuilles de propriétés de configuration, qui sont définies à l’aide de tables de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a04cf-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="a04cf-107">Pour plus d’informations sur la façon de travailler avec les tables d’affichage et de contrôler les objets, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a04cf-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a04cf-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a04cf-108">Header file:</span></span>  <br/> |<span data-ttu-id="a04cf-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a04cf-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a04cf-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a04cf-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a04cf-111">Objets de contrôle</span><span class="sxs-lookup"><span data-stu-id="a04cf-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="a04cf-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a04cf-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a04cf-113">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a04cf-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="a04cf-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a04cf-114">Called by:</span></span>  <br/> |<span data-ttu-id="a04cf-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="a04cf-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="a04cf-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a04cf-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a04cf-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="a04cf-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="a04cf-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a04cf-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a04cf-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="a04cf-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a04cf-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a04cf-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a04cf-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a04cf-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="a04cf-122">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédent.</span><span class="sxs-lookup"><span data-stu-id="a04cf-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="a04cf-123">Activate</span><span class="sxs-lookup"><span data-stu-id="a04cf-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="a04cf-124">Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération de programmation lorsqu’un utilisateur de l’application client clique sur le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="a04cf-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="a04cf-125">GetState</span><span class="sxs-lookup"><span data-stu-id="a04cf-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="a04cf-126">Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="a04cf-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a04cf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a04cf-127">See also</span></span>



[<span data-ttu-id="a04cf-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a04cf-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

