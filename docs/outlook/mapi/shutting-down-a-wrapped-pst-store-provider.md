---
title: Arrêt d'un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Dernière modification le: 02 juillet 2012'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409943"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="92b31-103">Arrêt d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="92b31-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92b31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92b31-105">Une fois que vous avez fini d'utiliser un fournisseur de magasins de fichiers de dossiers personnels (PST), vous devez arrêter correctement le fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="92b31-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="92b31-106">Pour plus d'informations sur l'utilisation du fournisseur de magasins PST encapsulé, consultez la rubrique [using a wrappedd PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="92b31-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="92b31-107">Pour arrêter un fournisseur de magasins PST encapsulé, vous devez appeler la fonction **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="92b31-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="92b31-108">Cette fonction ferme le fournisseur de magasins PST encapsulé de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="92b31-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="92b31-109">Dans cette rubrique, la fonction **IMSProvider:: Shutdown** est illustrée à l'aide d'un exemple de code à partir de l'exemple de fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="92b31-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="92b31-110">L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication.</span><span class="sxs-lookup"><span data-stu-id="92b31-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="92b31-111">Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="92b31-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="92b31-112">Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="92b31-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="92b31-113">Arrêter la routine</span><span class="sxs-lookup"><span data-stu-id="92b31-113">Shut Down Routine</span></span>

<span data-ttu-id="92b31-114">Le spouleur MAPI appelle la fonction **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** juste avant de libérer le fournisseur de magasins PST encapsulé afin que le fournisseur de magasins PST encapsulé puisse s'arrêter correctement.</span><span class="sxs-lookup"><span data-stu-id="92b31-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="92b31-115">La fonction met fin à tous les objets session associés au fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="92b31-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="92b31-116">CMSProvider:: ShutDown () exemple</span><span class="sxs-lookup"><span data-stu-id="92b31-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="92b31-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b31-117">See also</span></span>



[<span data-ttu-id="92b31-118">À propos de l'exemple de fournisseur de banque d'informations PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="92b31-119">Installation de l'exemple de fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="92b31-120">Initialisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="92b31-121">Connexion à un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="92b31-122">Utilisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="92b31-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

