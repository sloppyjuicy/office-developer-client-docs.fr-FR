---
title: Utilisation d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: eb32f8a6ca1b4fc2bf37221002b6a0080954984d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379548"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Utilisation d’un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016
  
Avant de pouvoir utiliser un fournisseur de magasin de dossiers personnels (PST) wrapped, vous devez initialiser et configurer le fournisseur de magasin PST wrapped. Une fois que le fournisseur de magasin PST wrapped est configuré, vous devez implémenter des fonctions afin que MAPI et lepooler MAPI peuvent se connecter au fournisseur de magasin de messages. Pour plus d’informations sur l’initialisation et la connexion à un fournisseur de magasins PST wrapped, voir [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md) and [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).
  
**[L’interface IMAPISupport::IUnknown](imapisupportiunknown.md)** fournit des implémentations pour les tâches couramment effectuées par les fournisseurs de magasins de messages. Cette interface doit être wrapped pour que le fournisseur de magasin PST Wrapped exemple fonctionne. La **[fonction IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** nécessite une implémentation spéciale. Toutes les autres fonctions peuvent transmettre leurs paramètres à l’objet wrapped sous-jacent.
  
Dans cette rubrique, la fonction **IMAPISupport::OpenProfileSection est démontrée** à l’aide d’un exemple de code du fournisseur de magasin PST Wrapped sample. L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST Wrapped, voir [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication](about-the-replication-api.md).
  
Lorsque vous avez terminé d’utiliser un fournisseur de magasin PST wrapped, vous devez arrêter correctement le fournisseur de magasin PST wrapped. Pour plus d’informations, [voir Shutting Down a Wrapped PST Store Provider](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Routine Ouvrir une section de profil

La **[fonction IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actuel. La fonction nécessite une gestion spéciale dans l’implémentation du fournisseur de magasin PST wrapped. Lorsque la fonction `pgNSTGlobalProfileSectionGuid` est demandée, elle renvoie la section de profil mise en cache.
  
### <a name="csupportopenprofilesection-example"></a>Exemple CSupport::OpenProfileSection()

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

## <a name="see-also"></a>Voir aussi

- [À propos de l’exemple de fournisseur de magasin PST wrapped](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l’exemple de fournisseur de magasin PST Wrapped](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisation d’un fournisseur de magasin PST wrapped](initializing-a-wrapped-pst-store-provider.md)
- [Connexion à un fournisseur de magasin PST wrapped](logging-on-to-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de magasin PST wrapped](shutting-down-a-wrapped-pst-store-provider.md)
