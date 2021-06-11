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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320152"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="be430-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="be430-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="be430-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be430-105">Obtient un pointeur vers un objet de magasin IMAP (Internet Message Access Protocol) non veloppé qui permet d’accéder au fichier PST (Personal Folders) sous-jacent sans avoir à demander la synchronisation et à télécharger les éléments.</span><span class="sxs-lookup"><span data-stu-id="be430-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="be430-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="be430-106">Parameters</span></span>

 <span data-ttu-id="be430-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="be430-107">_ppvObject_</span></span>
  
> <span data-ttu-id="be430-108">[out] Pointeur vers un objet de magasin [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) qui est déballé.</span><span class="sxs-lookup"><span data-stu-id="be430-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="be430-109">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="be430-109">Return values</span></span>

<span data-ttu-id="be430-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="be430-110">S_OK</span></span>
  
- <span data-ttu-id="be430-111">L’appel a réussi et un pointeur vers une interface non enveloppée a été renvoyé dans  _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="be430-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be430-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="be430-112">Remarks</span></span>

<span data-ttu-id="be430-113">Sans avoir d’abord désécrit un magasin IMAP, l’accès à un message dans la boutique peut forcer une synchronisation qui tente de télécharger l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="be430-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="be430-114">L’utilisation de la store non enveloppée permet d’accéder au message dans son état actuel sans déclencher de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="be430-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="be430-115">Étant donné que **UnwrapNoRef** n’incrémente pas le nombre de références pour ce nouveau pointeur vers l’objet store non enveloppé, après avoir correctement appelé **UnwrapNoRef,** vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour conserver le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="be430-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be430-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be430-116">See also</span></span>



[<span data-ttu-id="be430-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="be430-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

