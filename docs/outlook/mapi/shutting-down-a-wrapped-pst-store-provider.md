---
title: Arrêt d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: 43a65548bedc1729ff2bcb62bc3df78d2408bf12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571744"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a><span data-ttu-id="36c25-103">Arrêt d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-103">Shutting Down a Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="36c25-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36c25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36c25-105">Après avoir utilisant un fournisseur de magasin de dossiers personnels (PST) de fichier encapsulé, vous devez fermer correctement le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="36c25-105">After you finish using a wrapped Personal Folders file (PST) store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="36c25-106">Pour plus d’informations sur l’utilisation du fournisseur de magasin PST encapsulé, voir [utilisation d’un fournisseur de magasin encapsulé PST](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36c25-106">For more information about using the wrapped PST store provider, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="36c25-107">Pour arrêter un fournisseur de magasins PST encapsulé, vous devez appeler la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** .</span><span class="sxs-lookup"><span data-stu-id="36c25-107">To shut down a wrapped PST store provider, you must call the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function.</span></span> <span data-ttu-id="36c25-108">Ces fonctions ferme le fournisseur de banque PST justifié de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="36c25-108">This functions closes down the wrapped PST store provider in an orderly fashion.</span></span> 
  
<span data-ttu-id="36c25-109">Dans cette rubrique, la fonction **IMSProvider::Shutdown** est illustrée à l’aide d’un exemple de code à partir du fournisseur de magasin exemple encapsulé PST.</span><span class="sxs-lookup"><span data-stu-id="36c25-109">In this topic, the **IMSProvider::Shutdown** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="36c25-110">L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="36c25-110">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="36c25-111">Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36c25-111">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="36c25-112">Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="36c25-112">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="shut-down-routine"></a><span data-ttu-id="36c25-113">Arrêter de Routine</span><span class="sxs-lookup"><span data-stu-id="36c25-113">Shut Down Routine</span></span>

<span data-ttu-id="36c25-114">Le spouleur MAPI appelle la fonction **[IMSProvider::Shutdown](imsprovider-shutdown.md)** juste avant qu’il libère le fournisseur de banque PST encapsulé afin que le fournisseur de banque PST encapsulé peut s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="36c25-114">The MAPI spooler calls the **[IMSProvider::Shutdown](imsprovider-shutdown.md)** function just before it releases the wrapped PST store provider so that the wrapped PST store provider can shut down properly.</span></span> <span data-ttu-id="36c25-115">La fonction s’arrête tous les objets de session associés au fournisseur de magasin PST justifié.</span><span class="sxs-lookup"><span data-stu-id="36c25-115">The function terminates all session objects associated with the wrapped PST store provider.</span></span> 
  
## <a name="cmsprovidershutdown-example"></a><span data-ttu-id="36c25-116">Exemple CMSProvider::ShutDown()</span><span class="sxs-lookup"><span data-stu-id="36c25-116">CMSProvider::ShutDown() Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="36c25-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36c25-117">See also</span></span>



[<span data-ttu-id="36c25-118">À propos de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-118">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="36c25-119">Installation de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-119">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="36c25-120">Initialisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-120">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="36c25-121">Connexion à un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-121">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="36c25-122">Utilisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="36c25-122">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)

