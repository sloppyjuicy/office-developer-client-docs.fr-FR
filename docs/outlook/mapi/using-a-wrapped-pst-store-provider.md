---
title: À l’aide d’un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787440"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="544de-103">À l’aide d’un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="544de-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="544de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="544de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="544de-105">Avant de pouvoir utiliser un fournisseur de magasins encapsulé dossiers personnels (PST) de fichier, vous devez initialiser et configurer le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="544de-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="544de-106">Une fois que le fournisseur de banque PST encapsulé est configuré, vous devez implémenter les fonctions afin que MAPI et le spouleur MAPI peuvent se connecter au fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="544de-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="544de-107">Pour plus d’informations sur l’initialisation et de se connecter à un fournisseur de magasin PST encapsulé, voir [l’initialisation d’un fournisseur de magasin encapsulé PST](initializing-a-wrapped-pst-store-provider.md) et [l’enregistrement à un fournisseur de magasin encapsulé PST](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="544de-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="544de-108">L’interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** fournit des implémentations des tâches fréquemment effectuées par message stockent des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="544de-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="544de-109">Cette interface doit être entourée du exemple encapsulé PST magasin fournisseur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="544de-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="544de-110">La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requiert l’implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="544de-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="544de-111">Toutes les autres fonctions peuvent passer leurs paramètres à l’objet sous-jacent encapsulé.</span><span class="sxs-lookup"><span data-stu-id="544de-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="544de-112">Dans cette rubrique, la fonction **IMAPISupport::OpenProfileSection** est illustrée à l’aide d’un exemple de code à partir du fournisseur de magasin exemple encapsulé PST.</span><span class="sxs-lookup"><span data-stu-id="544de-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="544de-113">L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="544de-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="544de-114">Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="544de-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="544de-115">Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="544de-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="544de-116">Lorsque vous avez terminé à l’aide d’un fournisseur de magasins PST encapsulé, vous devez fermer correctement le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="544de-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="544de-117">Pour plus d’informations, voir [Arrêt un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="544de-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="544de-118">Routine Open Section de profil</span><span class="sxs-lookup"><span data-stu-id="544de-118">Open Profile Section routine</span></span>

<span data-ttu-id="544de-119">La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actuel.</span><span class="sxs-lookup"><span data-stu-id="544de-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="544de-120">La fonction nécessite un traitement spécial dans l’implémentation du fournisseur de magasin PST justifié.</span><span class="sxs-lookup"><span data-stu-id="544de-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="544de-121">Lors de la `pgNSTGlobalProfileSectionGuid` est demandé, la fonction renvoie la section profil qui est mis en cache.</span><span class="sxs-lookup"><span data-stu-id="544de-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="544de-122">Exemple CSupport::OpenProfileSection()</span><span class="sxs-lookup"><span data-stu-id="544de-122">CSupport::OpenProfileSection() example</span></span>

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a><span data-ttu-id="544de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="544de-123">See also</span></span>

- [<span data-ttu-id="544de-124">À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels</span><span class="sxs-lookup"><span data-stu-id="544de-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="544de-125">Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels</span><span class="sxs-lookup"><span data-stu-id="544de-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="544de-126">L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="544de-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="544de-127">Se connecter à un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="544de-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="544de-128">Arrêt d’un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="544de-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

