---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783792"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="95d43-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95d43-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="95d43-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95d43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95d43-105">Prend en charge l’utilisation des formulaires d’exécution configurables dans des environnements informatiques distribués.</span><span class="sxs-lookup"><span data-stu-id="95d43-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95d43-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="95d43-106">Header file:</span></span>  <br/> |<span data-ttu-id="95d43-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="95d43-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="95d43-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="95d43-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="95d43-109">Objets de fabrique de formulaire</span><span class="sxs-lookup"><span data-stu-id="95d43-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="95d43-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="95d43-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="95d43-111">Serveurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="95d43-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="95d43-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="95d43-112">Called by:</span></span>  <br/> |<span data-ttu-id="95d43-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="95d43-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="95d43-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="95d43-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="95d43-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="95d43-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="95d43-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="95d43-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="95d43-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="95d43-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="95d43-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="95d43-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="95d43-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="95d43-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="95d43-120">Renvoie un objet de fabrique de classe pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="95d43-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="95d43-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="95d43-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="95d43-122">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de fabrique de formulaire.</span><span class="sxs-lookup"><span data-stu-id="95d43-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="95d43-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="95d43-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="95d43-124">Tenir à jour un serveur de formulaire ouvert en mémoire.</span><span class="sxs-lookup"><span data-stu-id="95d43-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95d43-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="95d43-125">Remarks</span></span>

<span data-ttu-id="95d43-126">L’interface **IMAPIFormFactory** repose sur l’interface [IClassFactory](http://msdn.microsoft.com/fr-fr/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="95d43-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](http://msdn.microsoft.com/fr-fr/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="95d43-127">**IMAPIFormFactory** est l’interface visionneuses de formulaire permet de créer de nouveaux objets de formulaire lorsqu’un serveur de formulaire prend en charge plus d’une classe de message (autrement dit, plus d’un type d’objet de formulaire).</span><span class="sxs-lookup"><span data-stu-id="95d43-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95d43-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d43-128">See also</span></span>



[<span data-ttu-id="95d43-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="95d43-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

