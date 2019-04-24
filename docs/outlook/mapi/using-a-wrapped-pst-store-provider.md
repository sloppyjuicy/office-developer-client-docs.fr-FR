---
title: Utilisation d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Dernière modification: 03 juillet 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329686"
---
# <a name="using-a-wrapped-pst-store-provider"></a><span data-ttu-id="d3d98-103">Utilisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="d3d98-103">Using a wrapped PST store provider</span></span>

<span data-ttu-id="d3d98-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3d98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3d98-105">Avant de pouvoir utiliser un fournisseur de magasins de fichiers de dossiers personnels (PST), vous devez initialiser et configurer le fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="d3d98-105">Before you can use a wrapped Personal Folders file (PST) store provider, you must initialize and configure the wrapped PST store provider.</span></span> <span data-ttu-id="d3d98-106">Une fois le fournisseur de banque de fichiers PST encapsulé configuré, vous devez implémenter des fonctions afin que MAPI et le spouleur MAPI puissent se connecter au fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d3d98-106">After the wrapped PST store provider is configured, you must implement functions so that MAPI and the MAPI spooler can log on to the message store provider.</span></span> <span data-ttu-id="d3d98-107">Pour plus d'informations sur l'initialisation et la connexion à un fournisseur de magasins de dossiers personnels (PST) encapsulé, consultez [la rubrique initialisation d'un fournisseur de magasins](initializing-a-wrapped-pst-store-provider.md) de fichiers PST encapsulés et [connexion à un fournisseur de magasins de dossiers personnels](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d3d98-107">For more information about initializing and logging on to a wrapped PST store provider, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="d3d98-108">L'interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** fournit des implémentations pour les tâches couramment effectuées par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d3d98-108">The **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface provides implementations for tasks that are commonly performed by message store providers.</span></span> <span data-ttu-id="d3d98-109">Cette interface doit être incluse dans un wrapper pour que l'exemple de fournisseur de magasins PST encapsulé fonctionne.</span><span class="sxs-lookup"><span data-stu-id="d3d98-109">This interface must be wrapped for the Sample Wrapped PST Store Provider to work.</span></span> <span data-ttu-id="d3d98-110">La fonction **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** nécessite une implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="d3d98-110">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function requires special implementation.</span></span> <span data-ttu-id="d3d98-111">Toutes les autres fonctions peuvent transmettre leurs paramètres à l'objet encapsulé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d3d98-111">All other functions can pass their parameters to the underlying wrapped object.</span></span> 
  
<span data-ttu-id="d3d98-112">Dans cette rubrique, la fonction **IMAPISupport:: OpenProfileSection** est illustrée à l'aide d'un exemple de code à partir de l'exemple de fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="d3d98-112">In this topic, the **IMAPISupport::OpenProfileSection** function is demonstrated by using a code example from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="d3d98-113">L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication.</span><span class="sxs-lookup"><span data-stu-id="d3d98-113">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d3d98-114">Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d3d98-114">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="d3d98-115">Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="d3d98-115">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="d3d98-116">Une fois que vous avez terminé d'utiliser un fournisseur de magasins PST encapsulé, vous devez arrêter correctement le fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="d3d98-116">When you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span> <span data-ttu-id="d3d98-117">Pour plus d'informations, consultez la rubrique [arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d3d98-117">For more information, see [Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="open-profile-section-routine"></a><span data-ttu-id="d3d98-118">Ouvrir la routine de section de profil</span><span class="sxs-lookup"><span data-stu-id="d3d98-118">Open Profile Section routine</span></span>

<span data-ttu-id="d3d98-119">La fonction **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actif.</span><span class="sxs-lookup"><span data-stu-id="d3d98-119">The **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function opens a section of the current profile.</span></span> <span data-ttu-id="d3d98-120">La fonction nécessite un traitement spécial dans l'implémentation du fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="d3d98-120">The function requires special handling in the wrapped PST store provider implementation.</span></span> <span data-ttu-id="d3d98-121">Lorsque le `pgNSTGlobalProfileSectionGuid` est demandé, la fonction renvoie la section de profil mise en cache.</span><span class="sxs-lookup"><span data-stu-id="d3d98-121">When the  `pgNSTGlobalProfileSectionGuid` is requested, the function returns the profile section that is cached.</span></span> 
  
### <a name="csupportopenprofilesection-example"></a><span data-ttu-id="d3d98-122">CSupport:: OpenProfileSection () exemple</span><span class="sxs-lookup"><span data-stu-id="d3d98-122">CSupport::OpenProfileSection() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d3d98-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3d98-123">See also</span></span>

- [<span data-ttu-id="d3d98-124">À propos de l'exemple de fournisseur de banque d'informations PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="d3d98-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d3d98-125">Installation de l'exemple de fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="d3d98-125">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d3d98-126">Initialisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="d3d98-126">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d3d98-127">Connexion à un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="d3d98-127">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="d3d98-128">Arrêt d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="d3d98-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

