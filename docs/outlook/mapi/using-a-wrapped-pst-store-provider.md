---
title: Utilisation d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Dernière modification: 03 juillet 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420821"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Utilisation d’un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir utiliser un fournisseur de magasins de fichiers de dossiers personnels (PST), vous devez initialiser et configurer le fournisseur de magasins PST encapsulé. Une fois le fournisseur de banque de fichiers PST encapsulé configuré, vous devez implémenter des fonctions afin que MAPI et le spouleur MAPI puissent se connecter au fournisseur de banque de messages. Pour plus d'informations sur l'initialisation et la connexion à un fournisseur de magasins de dossiers personnels (PST) encapsulé, consultez [la rubrique initialisation d'un fournisseur de magasins](initializing-a-wrapped-pst-store-provider.md) de fichiers PST encapsulés et [connexion à un fournisseur de magasins de dossiers personnels](logging-on-to-a-wrapped-pst-store-provider.md).
  
L'interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** fournit des implémentations pour les tâches couramment effectuées par les fournisseurs de banque de messages. Cette interface doit être incluse dans un wrapper pour que l'exemple de fournisseur de magasins PST encapsulé fonctionne. La fonction **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** nécessite une implémentation spéciale. Toutes les autres fonctions peuvent transmettre leurs paramètres à l'objet encapsulé sous-jacent. 
  
Dans cette rubrique, la fonction **IMAPISupport:: OpenProfileSection** est illustrée à l'aide d'un exemple de code à partir de l'exemple de fournisseur de magasins PST encapsulé. L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication. Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.
  
Une fois que vous avez terminé d'utiliser un fournisseur de magasins PST encapsulé, vous devez arrêter correctement le fournisseur de magasins PST encapsulé. Pour plus d'informations, consultez la rubrique [arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Ouvrir la routine de section de profil

La fonction **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** ouvre une section du profil actif. La fonction nécessite un traitement spécial dans l'implémentation du fournisseur de magasins PST encapsulé. Lorsque le `pgNSTGlobalProfileSectionGuid` est demandé, la fonction renvoie la section de profil mise en cache. 
  
### <a name="csupportopenprofilesection-example"></a>CSupport:: OpenProfileSection () exemple

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

- [À propos de l'exemple de fournisseur de banque d'informations PST encapsulé](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
- [Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
- [Connexion à un fournisseur de magasins PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
- [Arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

