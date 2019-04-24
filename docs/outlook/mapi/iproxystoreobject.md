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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315518"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="87e9e-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="87e9e-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="87e9e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e9e-105">Fournit un objet de magasin IMAP (Internet Message Access Protocol) qui a été dévoilé et qui autorise l'accès à des éléments dans le fichier de dossiers personnels (PST) sans appeler la synchronisation et télécharger les éléments.</span><span class="sxs-lookup"><span data-stu-id="87e9e-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="87e9e-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="87e9e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87e9e-107">Hérité de:</span><span class="sxs-lookup"><span data-stu-id="87e9e-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="87e9e-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="87e9e-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="87e9e-109">Fourni par:</span><span class="sxs-lookup"><span data-stu-id="87e9e-109">Provided By:</span></span>  <br/> |<span data-ttu-id="87e9e-110">Fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="87e9e-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="87e9e-111">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="87e9e-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="87e9e-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="87e9e-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="87e9e-113">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="87e9e-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="87e9e-114">*Membre de l'espace réservé*</span><span class="sxs-lookup"><span data-stu-id="87e9e-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="87e9e-115">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="87e9e-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="87e9e-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="87e9e-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="87e9e-117">Obtient un pointeur vers un magasin IMAP non encapsulé.</span><span class="sxs-lookup"><span data-stu-id="87e9e-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="87e9e-118">*Membre de l'espace réservé*</span><span class="sxs-lookup"><span data-stu-id="87e9e-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="87e9e-119">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="87e9e-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87e9e-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="87e9e-120">Remarks</span></span>

<span data-ttu-id="87e9e-121">Appelez [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur la Banque de messages source pour obtenir l'interface **IProxyStoreObject** .</span><span class="sxs-lookup"><span data-stu-id="87e9e-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="87e9e-122">Appelez ensuite **IProxyStoreObject:: UnwrapNoRef** pour obtenir l'objet Store déenveloppé.</span><span class="sxs-lookup"><span data-stu-id="87e9e-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="87e9e-123">Si **QueryInterface** renvoie l'erreur **MAPI_E_INTERFACE_NOT_SUPPORTED**, cela signifie que la Banque n'a pas été incluse dans un wrapper.</span><span class="sxs-lookup"><span data-stu-id="87e9e-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="87e9e-124">Étant donné que **UnwrapNoRef** n'incrémente pas le décompte de référence pour ce nouveau pointeur vers l'objet Store non encapsulé, après avoir correctement appelé **UnwrapNoRef**, vous devez appeler [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour maintenir le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="87e9e-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

