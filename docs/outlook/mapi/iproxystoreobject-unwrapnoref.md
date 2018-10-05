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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382931"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="0c24a-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="0c24a-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="0c24a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c24a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c24a-105">Obtient un pointeur vers un objet banque IMAP Internet Message Access Protocol () non qui fournit l’accès dans le fichier de dossiers personnels (PST) sous-jacent sans appel de la synchronisation et de télécharger les éléments.</span><span class="sxs-lookup"><span data-stu-id="0c24a-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="0c24a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c24a-106">Parameters</span></span>

 <span data-ttu-id="0c24a-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="0c24a-107">_ppvObject_</span></span>
  
> <span data-ttu-id="0c24a-108">[out] Pointeur vers une [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet store qui est non.</span><span class="sxs-lookup"><span data-stu-id="0c24a-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0c24a-109">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0c24a-109">Return values</span></span>

<span data-ttu-id="0c24a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c24a-110">S_OK</span></span>
  
- <span data-ttu-id="0c24a-111">L’appel a réussi et un pointeur vers une interface non a été renvoyé dans _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="0c24a-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c24a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c24a-112">Remarks</span></span>

<span data-ttu-id="0c24a-113">Sans premier dévoilement une banque IMAP, l’accès à un message dans la banque peut de forcer une synchronisation qui tente de télécharger l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="0c24a-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="0c24a-114">À l’aide de la banque non permet d’accéder au message dans son état actuel sans déclencher un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="0c24a-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="0c24a-115">Étant donné que **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après la réussite de l’appel **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour maintenir le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="0c24a-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c24a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c24a-116">See also</span></span>



[<span data-ttu-id="0c24a-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="0c24a-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

