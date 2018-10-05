---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395307"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="06ee5-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="06ee5-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="06ee5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06ee5-105">Fournit un objet de banque IMAP Internet Message Access Protocol () qui a été non et qui permet d’accéder aux éléments dans le fichier de dossiers personnels (PST) sans appel de la synchronisation et de télécharger les éléments.</span><span class="sxs-lookup"><span data-stu-id="06ee5-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="06ee5-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="06ee5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06ee5-107">Hérité :</span><span class="sxs-lookup"><span data-stu-id="06ee5-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="06ee5-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="06ee5-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="06ee5-109">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="06ee5-109">Provided By:</span></span>  <br/> |<span data-ttu-id="06ee5-110">Fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="06ee5-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="06ee5-111">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="06ee5-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="06ee5-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="06ee5-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="06ee5-113">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="06ee5-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="06ee5-114">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="06ee5-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="06ee5-115">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="06ee5-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="06ee5-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="06ee5-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="06ee5-117">Obtient un pointeur vers une banque IMAP non.</span><span class="sxs-lookup"><span data-stu-id="06ee5-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="06ee5-118">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="06ee5-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="06ee5-119">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="06ee5-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06ee5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="06ee5-120">Remarks</span></span>

<span data-ttu-id="06ee5-121">Appeler [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur la banque de messages source pour obtenir l’interface **IProxyStoreObject** .</span><span class="sxs-lookup"><span data-stu-id="06ee5-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="06ee5-122">Appelez ensuite **IProxyStoreObject::UnwrapNoRef** pour obtenir l’objet store non.</span><span class="sxs-lookup"><span data-stu-id="06ee5-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="06ee5-123">Si **QueryInterface** renvoie l’erreur **MAPI_E_INTERFACE_NOT_SUPPORTED**, puis la banque n’a pas été encapsulée.</span><span class="sxs-lookup"><span data-stu-id="06ee5-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="06ee5-124">Étant donné que **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après la réussite de l’appel **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour maintenir le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="06ee5-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

