---
title: Utilisation d’un fournisseur d’archive PST encapsulée
description: Décrit comment utiliser un fournisseur de magasins PST (Personal Folders File) encapsulé dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
ms.openlocfilehash: bfa353b907b64868f0d867e3dc39842c1130bbfe
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894626"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Utilisation d’un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016
  
Avant de pouvoir utiliser un fournisseur de magasin de fichiers PST (Personal Folders) encapsulé, vous devez initialiser et configurer le fournisseur de magasin PST encapsulé. Une fois le fournisseur de magasin PST encapsulé configuré, vous devez implémenter des fonctions afin que MAPI et le spouleur MAPI puissent se connecter au fournisseur du magasin de messages. Pour plus d’informations sur l’initialisation et la connexion à un fournisseur de magasin PST encapsulé, consultez [Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md) et connexion [à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md).
  
**[L’interface IMAPISupport::IUnknown](imapisupportiunknown.md)** fournit des implémentations pour les tâches qui sont généralement effectuées par les fournisseurs de magasins de messages. Cette interface doit être encapsulée pour que l’exemple de fournisseur du magasin PST encapsulé fonctionne. La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** nécessite une implémentation spéciale. Toutes les autres fonctions peuvent passer leurs paramètres à l’objet encapsulé sous-jacent.
  
Dans cette rubrique, la fonction **IMAPISupport::OpenProfileSection** est illustrée à l’aide d’un exemple de code de l’exemple de fournisseur de magasin PST encapsulé. L’exemple implémente un fournisseur PST encapsulé qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST encapsulé, consultez [l’installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez [À propos de l’API de réplication](about-the-replication-api.md).
  
Lorsque vous avez terminé d’utiliser un fournisseur de magasin PST encapsulé, vous devez arrêter correctement le fournisseur de magasin PST encapsulé. Pour plus d’informations, consultez [Arrêter un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Ouvrir la routine de la section Profil

La fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actuel. La fonction nécessite une gestion spéciale dans l’implémentation du fournisseur de magasin PST encapsulé. Lorsque la `pgNSTGlobalProfileSectionGuid` demande est demandée, la fonction retourne la section de profil mise en cache.
  
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

- [À propos de l’exemple de fournisseur de magasin PST encapsulé](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
- [Connexion à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
