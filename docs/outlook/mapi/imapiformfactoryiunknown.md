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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342118"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="29ca1-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29ca1-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="29ca1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29ca1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29ca1-105">Prend en charge l’utilisation de formulaires d’utilisation configurables dans les environnements informatiques distribués.</span><span class="sxs-lookup"><span data-stu-id="29ca1-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29ca1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="29ca1-106">Header file:</span></span>  <br/> |<span data-ttu-id="29ca1-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="29ca1-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="29ca1-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="29ca1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="29ca1-109">Objets fabrique de formulaires</span><span class="sxs-lookup"><span data-stu-id="29ca1-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="29ca1-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="29ca1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="29ca1-111">Serveurs de formulaires</span><span class="sxs-lookup"><span data-stu-id="29ca1-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="29ca1-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="29ca1-112">Called by:</span></span>  <br/> |<span data-ttu-id="29ca1-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="29ca1-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="29ca1-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="29ca1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="29ca1-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="29ca1-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="29ca1-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="29ca1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="29ca1-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="29ca1-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="29ca1-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="29ca1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="29ca1-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="29ca1-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="29ca1-120">Renvoie un objet fabrique de classes pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="29ca1-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="29ca1-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="29ca1-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="29ca1-122">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de fabrique de formulaire.</span><span class="sxs-lookup"><span data-stu-id="29ca1-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="29ca1-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="29ca1-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="29ca1-124">Conserve un serveur de formulaire ouvert en mémoire.</span><span class="sxs-lookup"><span data-stu-id="29ca1-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ca1-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="29ca1-125">Remarks</span></span>

<span data-ttu-id="29ca1-126">**L’interface IMAPIFormFactory** est basée sur l’interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="29ca1-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="29ca1-127">**IMAPIFormFactory** est l’interface que les visionneuses de formulaires utilisent pour créer des objets de formulaire lorsqu’un serveur de formulaires prend en charge plusieurs classes de message (c’est-à-dire, plusieurs types d’objet de formulaire).</span><span class="sxs-lookup"><span data-stu-id="29ca1-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29ca1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29ca1-128">See also</span></span>



[<span data-ttu-id="29ca1-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="29ca1-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

