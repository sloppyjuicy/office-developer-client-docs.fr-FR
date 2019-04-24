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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342174"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="98112-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="98112-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="98112-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98112-105">Renvoie un objet de fabrique de classe pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="98112-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="98112-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98112-106">Parameters</span></span>

 <span data-ttu-id="98112-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="98112-107">_clsidForm_</span></span>
  
> <span data-ttu-id="98112-108">dans Identificateur de classe du formulaire à créer par la fabrique de classes.</span><span class="sxs-lookup"><span data-stu-id="98112-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="98112-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98112-109">_ulFlags_</span></span>
  
> <span data-ttu-id="98112-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="98112-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="98112-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="98112-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="98112-112">remarquer Pointeur vers l'objet de fabrique de classes.</span><span class="sxs-lookup"><span data-stu-id="98112-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98112-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98112-113">Return value</span></span>

<span data-ttu-id="98112-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="98112-114">S_OK</span></span> 
  
> <span data-ttu-id="98112-115">L'objet de fabrique de classe a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="98112-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98112-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="98112-116">Remarks</span></span>

<span data-ttu-id="98112-117">Les visionneuses de formulaires appellent la méthode **IMAPIFormFactory:: CreateClassFactory** pour obtenir une fabrique de classe pour un formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="98112-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="98112-118">La fabrique de classe est utilisée pour créer des instances d'un formulaire qui gère les messages d'une classe spécifique et pour contrôler l'accès à ces instances.</span><span class="sxs-lookup"><span data-stu-id="98112-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="98112-119">La méthode **CreateClassFactory** est appelée par les visionneuses de formulaire pour obtenir un objet de fabrique de classe pour les serveurs de formulaires qui implémentent plusieurs classes de message.</span><span class="sxs-lookup"><span data-stu-id="98112-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="98112-120">Cette méthode reçoit un identificateur de classe (CLSID) en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="98112-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="98112-121">En fonction de ce paramètre, cette méthode peut déterminer le type spécifique de l'objet Factory de classe à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="98112-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="98112-122">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="98112-122">Notes to implementers</span></span>

<span data-ttu-id="98112-123">Vous pouvez revenir de votre implémentation **CreateClassFactory** le même objet de fabrique de classes sur plusieurs appels pour le même identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="98112-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="98112-124">La création d'une nouvelle instance de fabrique de classes n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="98112-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="98112-125">Vous pouvez avoir une seule implémentation de fabrique de classe qui crée des instances de fabrique de classe appropriées sur demande ou plusieurs implémentations de fabrique de classe, une pour chaque classe de message.</span><span class="sxs-lookup"><span data-stu-id="98112-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98112-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98112-126">See also</span></span>



[<span data-ttu-id="98112-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98112-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

