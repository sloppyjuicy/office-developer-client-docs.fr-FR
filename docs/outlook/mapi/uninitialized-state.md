---
title: État non initialisé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425560"
---
# <a name="uninitialized-state"></a><span data-ttu-id="7e3ec-103">État non initialisé</span><span class="sxs-lookup"><span data-stu-id="7e3ec-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="7e3ec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e3ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e3ec-105">L'état non initialisé est les objets de formulaire d'état initial doivent se trouver lors de leur création initiale.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="7e3ec-106">Les objets Form sont initialisés avec les données de message lorsqu'une application cliente appelle la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) sur l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="7e3ec-107">Le tableau suivant décrit les transitions autorisées à partir de l'État unitialized.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="7e3ec-108">**Méthode IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="7e3ec-108">**IPersistMessage method**</span></span>|<span data-ttu-id="7e3ec-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="7e3ec-109">**Action**</span></span>|<span data-ttu-id="7e3ec-110">**Nouvel État**</span><span class="sxs-lookup"><span data-stu-id="7e3ec-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e3ec-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="7e3ec-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="7e3ec-112">Charge l'objet Form avec les données par défaut.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="7e3ec-113">Normal</span><span class="sxs-lookup"><span data-stu-id="7e3ec-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="7e3ec-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="7e3ec-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="7e3ec-115">Charge l'objet Form avec les données du message cible.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="7e3ec-116">Normal</span><span class="sxs-lookup"><span data-stu-id="7e3ec-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="7e3ec-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="7e3ec-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="7e3ec-118">Renvoyer la valeur Success ou définir la dernière erreur sur et renvoyer E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7e3ec-119">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="7e3ec-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="7e3ec-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7e3ec-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="7e3ec-121">Renvoyer la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="7e3ec-122">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="7e3ec-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="7e3ec-123">Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces</span><span class="sxs-lookup"><span data-stu-id="7e3ec-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="7e3ec-124">Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7e3ec-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="7e3ec-125">Non initialisée</span><span class="sxs-lookup"><span data-stu-id="7e3ec-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e3ec-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e3ec-126">See also</span></span>



[<span data-ttu-id="7e3ec-127">État normal</span><span class="sxs-lookup"><span data-stu-id="7e3ec-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="7e3ec-128">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="7e3ec-128">Form States</span></span>](form-states.md)

