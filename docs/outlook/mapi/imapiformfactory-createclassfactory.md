---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572157"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="0d3d8-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="0d3d8-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="0d3d8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d3d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d3d8-105">Renvoie un objet de fabrique de classe pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="0d3d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d3d8-106">Parameters</span></span>

 <span data-ttu-id="0d3d8-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="0d3d8-107">_clsidForm_</span></span>
  
> <span data-ttu-id="0d3d8-108">[in] Un identificateur de classe pour le formulaire doit être créé à la fabrique de classe.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="0d3d8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d3d8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0d3d8-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0d3d8-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="0d3d8-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="0d3d8-112">[out] Pointeur vers l’objet de fabrique de classe.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d3d8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d3d8-113">Return value</span></span>

<span data-ttu-id="0d3d8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d3d8-114">S_OK</span></span> 
  
> <span data-ttu-id="0d3d8-115">L’objet de fabrique de classe a été retournée.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d3d8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d3d8-116">Remarks</span></span>

<span data-ttu-id="0d3d8-117">Visionneuses de formulaire appeler la méthode **IMAPIFormFactory::CreateClassFactory** pour obtenir une fabrique de classe pour un formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="0d3d8-118">La fabrique de classe est utilisée pour créer des instances d’un formulaire qui gère les messages d’une classe spécifique et pour contrôler l’accès à ces instances.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="0d3d8-119">La méthode **CreateClassFactory** est appelée par les visionneuses de formulaire pour obtenir un objet de fabrique de classe pour les serveurs de formulaire qui implémentent plusieurs classes de message.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="0d3d8-120">Cette méthode reçoit un identificateur de classe (CLSID) en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="0d3d8-121">En fonction de ce paramètre, cette méthode peut déterminer le type spécifique de l’objet de fabrique de classe à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0d3d8-122">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="0d3d8-122">Notes to implementers</span></span>

<span data-ttu-id="0d3d8-123">Vous pouvez renvoyer à partir de votre implémentation **CreateClassFactory** le même objet de fabrique de classe sur plusieurs appels pour le même identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="0d3d8-124">Création d’une nouvelle instance de fabrique de classe n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="0d3d8-125">Vous pouvez avoir une implémentation de fabrique de classe unique qui crée des instances de fabrique de classe appropriée à la demande ou de plusieurs implémentations de fabrique de classe, un pour chaque classe de message.</span><span class="sxs-lookup"><span data-stu-id="0d3d8-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d3d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d3d8-126">See also</span></span>



[<span data-ttu-id="0d3d8-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d3d8-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

