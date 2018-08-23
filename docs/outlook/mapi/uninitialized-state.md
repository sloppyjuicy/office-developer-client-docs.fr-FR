---
title: État non initialisé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578247"
---
# <a name="uninitialized-state"></a><span data-ttu-id="53247-103">État non initialisé</span><span class="sxs-lookup"><span data-stu-id="53247-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="53247-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53247-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53247-105">L’état non initialisée est le formulaire état initial dans des objets doivent être lors de leur création.</span><span class="sxs-lookup"><span data-stu-id="53247-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="53247-106">Objets de formulaire devient initialisés avec les données de message lorsqu’une application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) sur l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="53247-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="53247-107">Le tableau suivant décrit les transitions autorisées à partir de l’état Unitialized.</span><span class="sxs-lookup"><span data-stu-id="53247-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="53247-108">**Méthode IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="53247-108">**IPersistMessage method**</span></span>|<span data-ttu-id="53247-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="53247-109">**Action**</span></span>|<span data-ttu-id="53247-110">**Nouvel état**</span><span class="sxs-lookup"><span data-stu-id="53247-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="53247-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="53247-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="53247-112">Chargement de l’objet de formulaire avec des données par défaut.</span><span class="sxs-lookup"><span data-stu-id="53247-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="53247-113">Normal</span><span class="sxs-lookup"><span data-stu-id="53247-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="53247-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="53247-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="53247-115">Chargement de l’objet de formulaire avec des données à partir du message cible.</span><span class="sxs-lookup"><span data-stu-id="53247-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="53247-116">Normal</span><span class="sxs-lookup"><span data-stu-id="53247-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="53247-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="53247-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="53247-118">Renvoyez réussite, ou bien la dernière erreur et E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="53247-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="53247-119">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="53247-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="53247-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="53247-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="53247-121">Renvoie la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="53247-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="53247-122">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="53247-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="53247-123">Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces</span><span class="sxs-lookup"><span data-stu-id="53247-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="53247-124">Définissez la dernière erreur à et E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="53247-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="53247-125">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="53247-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53247-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53247-126">See also</span></span>



[<span data-ttu-id="53247-127">État normal</span><span class="sxs-lookup"><span data-stu-id="53247-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="53247-128">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="53247-128">Form States</span></span>](form-states.md)

