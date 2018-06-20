---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7c6c763e918947c423c5dae283b0d4ab2f880616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784397"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="90663-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="90663-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="90663-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90663-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90663-105">Obtient un pointeur vers un objet banque IMAP Internet Message Access Protocol () non qui fournit l’accès dans le fichier de dossiers personnels (PST) sous-jacent sans appel de la synchronisation et de télécharger les éléments.</span><span class="sxs-lookup"><span data-stu-id="90663-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="90663-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90663-106">Parameters</span></span>

 <span data-ttu-id="90663-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="90663-107">_ppvObject_</span></span>
  
> <span data-ttu-id="90663-108">[out] Pointeur vers une [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet store qui est non.</span><span class="sxs-lookup"><span data-stu-id="90663-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="90663-109">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="90663-109">Return values</span></span>

<span data-ttu-id="90663-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="90663-110">S_OK</span></span>
  
- <span data-ttu-id="90663-111">L’appel a réussi et un pointeur vers une interface non a été renvoyé dans _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="90663-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90663-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="90663-112">Remarks</span></span>

<span data-ttu-id="90663-113">Sans premier dévoilement une banque IMAP, l’accès à un message dans la banque peut de forcer une synchronisation qui tente de télécharger l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="90663-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="90663-114">À l’aide de la banque non permet d’accéder au message dans son état actuel sans déclencher un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="90663-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="90663-115">Étant donné que **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après la réussite de l’appel **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) pour maintenir le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="90663-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90663-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90663-116">See also</span></span>



[<span data-ttu-id="90663-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="90663-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

