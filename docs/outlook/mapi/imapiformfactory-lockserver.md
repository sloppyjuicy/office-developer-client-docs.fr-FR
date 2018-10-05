---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389056"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="556d1-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="556d1-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="556d1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="556d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="556d1-105">Tenir à jour un serveur de formulaire ouvert en mémoire.</span><span class="sxs-lookup"><span data-stu-id="556d1-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="556d1-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="556d1-106">Parameters</span></span>

 <span data-ttu-id="556d1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="556d1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="556d1-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="556d1-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="556d1-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="556d1-109">_fLockServer_</span></span>
  
> <span data-ttu-id="556d1-110">[in] **true** pour augmenter le nombre de verrous ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="556d1-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="556d1-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="556d1-111">Return value</span></span>

<span data-ttu-id="556d1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="556d1-112">S_OK</span></span> 
  
> <span data-ttu-id="556d1-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="556d1-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="556d1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="556d1-114">Remarks</span></span>

<span data-ttu-id="556d1-115">Visionneuses de formulaire appeler la méthode **IMAPIFormFactory::LockServer** pour conserver une application de serveur de formulaire ouvert en mémoire.</span><span class="sxs-lookup"><span data-stu-id="556d1-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="556d1-116">Conserver le serveur du formulaire en mémoire améliore ses performances lorsque les formulaires sont souvent créés et publiés.</span><span class="sxs-lookup"><span data-stu-id="556d1-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="556d1-117">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="556d1-117">Notes to implementers</span></span>

<span data-ttu-id="556d1-118">La méthode **IMAPIFormFactory::LockServer** est très similaire à la méthode [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="556d1-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="556d1-119">En fait, la méthode **IMAPIFormFactory::LockServer** gère un décompte de combien de fois qu’il a été appelé ; dans la mesure où ce nombre est supérieur à 0, la méthode empêche le serveur de formulaire déchargé de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="556d1-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="556d1-120">Vous pouvez utiliser la fonction [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) pour mettre en place.</span><span class="sxs-lookup"><span data-stu-id="556d1-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="556d1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="556d1-121">See also</span></span>



[<span data-ttu-id="556d1-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="556d1-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

