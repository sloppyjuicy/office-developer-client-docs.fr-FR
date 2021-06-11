---
title: Arrêt d’un fournisseur de magasin PST wrapped
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409943"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="87c2d-103">Arrêt d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="87c2d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c2d-105">Une fois que vous avez terminé d’utiliser un fournisseur de magasin de dossiers personnels (PST) wrapped, vous devez arrêter correctement le fournisseur de magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="87c2d-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="87c2d-106">Pour plus d’informations sur l’utilisation du fournisseur de magasin PST [wrapped, voir Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="87c2d-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="87c2d-107">Pour arrêter un fournisseur de magasin PST wrapped, vous devez appeler la **[fonction IMSProvider::Shutdown.](imsprovider-shutdown.md)**</span><span class="sxs-lookup"><span data-stu-id="87c2d-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="87c2d-108">Cette fonction ferme le fournisseur de magasin PST wrapped de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="87c2d-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="87c2d-109">Dans cette rubrique, la fonction **IMSProvider::Shutdown** est démontrée à l’aide d’un exemple de code du fournisseur de magasin PST Wrapped sample.</span><span class="sxs-lookup"><span data-stu-id="87c2d-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="87c2d-110">L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="87c2d-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="87c2d-111">Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST [Wrapped, voir Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="87c2d-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="87c2d-112">Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="87c2d-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="87c2d-113">Shut Down Routine</span><span class="sxs-lookup"><span data-stu-id="87c2d-113">Shut Down Routine</span></span>

<span data-ttu-id="87c2d-114">Lepooler MAPI appelle la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** juste avant de libérer le fournisseur de magasin PST wrapped afin que le fournisseur de magasin PST wrapped puisse s’arrêter correctement.</span><span class="sxs-lookup"><span data-stu-id="87c2d-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="87c2d-115">La fonction met fin à tous les objets de session associés au fournisseur de magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="87c2d-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="87c2d-116">Exemple CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="87c2d-116">CMSProvider::ShutDown() Example</span></span>

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a><span data-ttu-id="87c2d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c2d-117">See also</span></span>



[<span data-ttu-id="87c2d-118">À propos de l’exemple de fournisseur de magasins PST wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="87c2d-119">Installation de l’exemple de fournisseur de magasin PST Wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="87c2d-120">Initialisation d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="87c2d-121">Connexion à un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="87c2d-122">Utilisation d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="87c2d-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

