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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783699"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="51e2e-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51e2e-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="51e2e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51e2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51e2e-105">Permet de désactive un contrôle bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé.</span><span class="sxs-lookup"><span data-stu-id="51e2e-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="51e2e-106">Fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que des feuilles de propriétés de configuration, qui sont définies à l’aide de tables de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="51e2e-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="51e2e-107">Pour plus d’informations sur la façon de travailler avec les tables d’affichage et de contrôler les objets, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="51e2e-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51e2e-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="51e2e-108">Header file:</span></span>  <br/> |<span data-ttu-id="51e2e-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51e2e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="51e2e-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="51e2e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="51e2e-111">Objets de contrôle</span><span class="sxs-lookup"><span data-stu-id="51e2e-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="51e2e-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="51e2e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="51e2e-113">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="51e2e-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="51e2e-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="51e2e-114">Called by:</span></span>  <br/> |<span data-ttu-id="51e2e-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="51e2e-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="51e2e-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="51e2e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="51e2e-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="51e2e-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="51e2e-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="51e2e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="51e2e-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="51e2e-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="51e2e-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="51e2e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="51e2e-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="51e2e-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="51e2e-122">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédent.</span><span class="sxs-lookup"><span data-stu-id="51e2e-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="51e2e-123">Activate</span><span class="sxs-lookup"><span data-stu-id="51e2e-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="51e2e-124">Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération de programmation lorsqu’un utilisateur de l’application client clique sur le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="51e2e-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="51e2e-125">GetState</span><span class="sxs-lookup"><span data-stu-id="51e2e-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="51e2e-126">Récupère une valeur qui indique si le contrôle bouton est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="51e2e-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51e2e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51e2e-127">See also</span></span>



[<span data-ttu-id="51e2e-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="51e2e-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

