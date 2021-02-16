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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414038"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="408fc-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="408fc-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="408fc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="408fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="408fc-105">Active et désactive un contrôle de bouton et effectue des tâches lorsqu’un utilisateur d’une application cliente clique sur le contrôle activé.</span><span class="sxs-lookup"><span data-stu-id="408fc-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="408fc-106">Les fournisseurs de services implémentent des objets de contrôle pour créer des boutons personnalisés dans les boîtes de dialogue, tels que les feuilles de propriétés de configuration, qui sont définis à l’aide de tableaux d’affichage.</span><span class="sxs-lookup"><span data-stu-id="408fc-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="408fc-107">Pour plus d’informations sur l’emploi de tableaux d’affichage et d’objets de contrôle, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="408fc-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="408fc-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="408fc-108">Header file:</span></span>  <br/> |<span data-ttu-id="408fc-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="408fc-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="408fc-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="408fc-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="408fc-111">Objets de contrôle</span><span class="sxs-lookup"><span data-stu-id="408fc-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="408fc-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="408fc-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="408fc-113">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="408fc-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="408fc-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="408fc-114">Called by:</span></span>  <br/> |<span data-ttu-id="408fc-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="408fc-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="408fc-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="408fc-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="408fc-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="408fc-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="408fc-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="408fc-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="408fc-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="408fc-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="408fc-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="408fc-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="408fc-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="408fc-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="408fc-122">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédente.</span><span class="sxs-lookup"><span data-stu-id="408fc-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="408fc-123">Activate</span><span class="sxs-lookup"><span data-stu-id="408fc-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="408fc-124">Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programme lorsqu’un utilisateur de l’application cliente clique sur le contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="408fc-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="408fc-125">GetState</span><span class="sxs-lookup"><span data-stu-id="408fc-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="408fc-126">Extrait une valeur qui indique si le contrôle de bouton est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="408fc-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="408fc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="408fc-127">See also</span></span>



[<span data-ttu-id="408fc-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="408fc-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

